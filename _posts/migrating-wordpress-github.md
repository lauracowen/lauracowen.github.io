---
layout: post
title:  "Migrating from Wordpress to GitHub Pages"
date:   2019-10-31 15:19:29 -0500
categories: 
---

Assumes you understand and are happy using:
GitHub installed and an use
Wordpress plugins (installing new ones) and using dashboard
Docker installed and the basics (though commands you need are given)


== Docker
Docker container for running Jekyll locally without installing it:
https://github.com/envygeeks/jekyll-docker/blob/master/README.md#standard (standard/default one is fine)


Create a directory to contain the site (eg `/home/laura/website/`).
Create a new Jekyll site using the Docker container (in a dir called `myblog` - doesn't matter what you call it as it's just a local directory - won't go on github):
`docker run --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll:3.8 jekyll new myblog`

Now run it:
`docker run --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll:3.8 jekyll serve`


Go to:
`http://localhost:4000/`

Ta-da!


You can edit the values of the title, email, description:, and twitter/github usernames now but leave the other values as they are. Save `config.yaml` then CTRL+C and docker run to pick up your changes.

=== Performance improvement

You'll notice that the docker container installs a load of gems before actually starting the server. When working on the website, you can add/change/remove individual pages without restarting the server, but for any config changes (which you'll do a lot at the start), you'll need to keep killing and restarting the server. So it's worth caching these gem installations, you can do this by instead using this run command, which mounts a second location into which the gems are installed the first time you run the container but then aren't reinstalled each time you run the container subsequently:

`mkdir ../bundle-cache`

`docker run --rm --volume="$PWD:/srv/jekyll" --volume="$PWD/../bundle-cache:/usr/local/bundle" -p 4000:4000 -it jekyll/jekyll:3.8 jekyll serve`

(you'll thank me later, as I thanked @fraz3alpha who advised me to do this)


== Export posts from Wordpress

In Wordpress dashboard, run backups (eg Dropbox Backup & Restore and Tools > Export at least to grab the text of your posts). Tho not doing anything to the site so this is just a usual precaution.

Disable all plugins if you can, at least just temporarily.

Install 'WordPress to Jekyll Exporter' plugin by Ben Balter. Then Tools > Export > Export to Jekyll. This creates a nice zip file containing all your posts as markdown that you can download.

Extract the zip file locally. Although Ben's exporter creates a nice little site structure, it's easier just to use the default Jekyll site you created above and copy the exported blog post files into that. In the `_posts` directory, select all the posts and copy/paste them into the `_posts` directory in your new Jekyll site. Docker/Jekyll should automatically regenerate the site. Ta-da! (again)

The images are currently pulled in from your existing Wordpress site but we'll deal with that later.


== Fix up the URLs

The post files each has a `permalink` entry in its front matter, which is useful because this means it's fairly easy to ensure that you don't break the original links.

=== Removing .html suffixes by default

In my Wordpress installation, my URLs are of the format: `http://lauracowen.co.uk/blog/2016/01/02/i-love-parkrun/` not `http://lauracowen.co.uk/blog/2016/01/02/i-love-parkrun.html`, as Jeykll does automatically. The only reason the posts aren't displaying with `.html` in the new site is because of the `permalink` entry at the top of each file. New posts, unless you include a `permalink` in every file, will by default have `.html` suffixes. I didn't want this.

Open `config.yaml` and add to the end of it `permalink: /:year/:month/:day/:title/`. CTRL+C and docker run to pick up the changes.

=== Including `/blog` prefixes

Also notice my WP URLs have the string `/blog` after the domain and before the post-specific part of the URL (eg `/blog/2016/01/02/i-love-parkrun/`, not `/2016/01/02/i-love-parkrun`). Can easily set this for the whole site by setting the `baseurl` in the config.yaml.

Don't touch the `url` value though or you won't be able to view the site locally. check this

=== Including `/blog` prefix only on blog posts


On WP, `http://lauracowen.co.uk/` redirects to `http://lauracowen.co.uk/blog/`. On GitHub, I'd like to have only the blog posts in the `/blog` sub-dir and anything else at a higher level. To do this, we need to group files within the site according to 'collections'. https://jekyllrb.com/docs/collections/

```
#permalink: /:year/:month/:day/:title/

collections:
  test:
    output: true
    permalink: /gubbins/:title/
  posts:
    output: true
    permalink: /blog/:year/:month/:day/:title/
```
Also, set `baseurl: ""` (default of nothing).

This means the site by default doesn't have any sub-dir after the domain part of the URL before the page-specific URL. But for blog posts specifically, the files in the `_posts` directory (collection `posts` maps automatically to the directory `_posts`) have the permalink that includes `/blog` prefix.

`permalink` entry in individual post files overrides this config setting so either need to remove the line from the front matter, or do as I did and update it to match the default config. I did the latter because it was important that the original URL from the WP site was retained, even if I went messing with the config file some more and changed something else accidentally breaking it.

So move into the `_posts` directory then run:

`sed --in-place -e 's/permalink: /permalink: \/blog/' *.md` (before running it against `*.md`, try it on a single file name first to to check it works)


== Push to GitHub and check as GitHub Pages

GitHub: create a new repo but don't check any boxes to create any files in the repo - it must stay empty or you'll have problems when you try to commit your files.

Locally, `git init` then `git remote add origin git@github.com:lauracowen/lauracowen.github.io.git` (address of repo is from the repo creation page so don't close it after creating repo). `git remote -v` to check. I use ssh not username/pw (you should too - link) so URL might be slightly different format.

`git status`

`git add --all` (or just selectively add a couple of your posts if you want to take the opportunity for a cleanout before pushing them all to a public GH repo) Jekyll created a `.gitignore` file for you so that helps.

`git commit -m "Initial migration from Wordpress"`

`git config --global user.email "lauracowen@users.noreply.github.com`

`git config --global user.name "lauracowen"`

`git push`

Pushes to `master` branch.

GitHub automatically rebuilds and publishes at `https://lauracowen.github.io/`.

At this point, I noticed my images hadn't copied down from WP.



== Export media from Wordpress

My Wordpress host, Clook.net, provides cPanel so I can use the browser-based file manager to zip up and download the `uploads` directory. There are WP plugins to export media but they needed a newer version of PHP than I have installed so I didn't try them (search for new plugins with something like 'export media').

Took the opportunity to delete a load of my old blog posts that are of no interest to anyone any more. That left me with 44 posts, of which some have images. Some images I just don't have any more because I lost access to the online gallery that I linked to. Where the images were stored directly in Wordpress, I had lost a few random images probably when migrating between Wordpress instances when I moved hosting a few years ago. Of what's left, I decided it was easiest to just manually work through the directories of images, delete the many differently sized versions that WP generates, and edit the posts with correct markdown syntax links.

Jekyll doesn't recognise sub-directories of image files in the `_posts` directory. You need to create a directory in the root of the project (eg `assets`) which Jekyll then pulls in. To reference an image from a post, you then use the format `![alt text](/assets/image_name.png)` - the slash (`/`) before `assets` is important because it tells Jekyll that the `assets` directory is in the root of the project. I used a `sed` command again to update the references to image files from my posts.

== Export comments from Wordpress

(don't take Wordpress site down until everything's done)

https://girliemac.com/blog/2013/12/27/wordpress-to-jekyll/

https://help.disqus.com/en/articles/1935528-jekyll-installation-instructions


== Things not yet working

* Embedded pins from Pinterest
* Embedded slides from Slideshare(?)
