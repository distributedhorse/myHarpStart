# Harp boilerplate / starter pack

## harp init --boilerplate

This is a barely-there starter for [Harp](http://harpjs.com/docs/environment/init). It uses SASS instead of LESS. And includes `normalize.css` and slightly more in the `head` than the one Harp gives you with a basic:

    harp init

Otherwise, the only other difference is the addition of a folder called `DELETE-AFTER-READING` which you can safely delete if you don't need it. The `DELETE-AFTER-READING` contains reference code for:

- setting up a simple blog / post loop with an RSS feed and a sitemap
- using mutliple layouts 

If you don't need either of these, just delete the folder and the `posts` folder. I use this as a starter pack for prototyping so it's sometimes useful to be able to play with more than one main template / JS configurations. Or to have radically different CSS approaches.

More about the blog and the different layouts below.

## How to set up a Harp project using this boilerplate

To use this enter following at command line (after reading the link above):

    harp init your-project-name --boilerplate i41/myHarpStart

## Adding new styles and stylesheets

If you create new SASS files you should add them to `_all.scss` and they'll be imported into `main.scss`. Or you can just add SASS / CSS directly into `main.scss`.

## Adding new pages

Harp expects pages to be in the `public` folder. You can create new folders inside that to create a tree / directory structure as you would normally. Anything that has the path `public/folder` will be served at `/folder`.

You can add pages as HTML, jade or markdown. And they'll be magically transformed into HTML. The header / footer / stylesheet information is all in `public/_layout.jade`. There's comments in this file which gives an indication of where to change stuff.

Partials are in the `public/_shared` folder unless I wasn't thinking too carefully.

## Adding new blog posts

You create new blog posts in the `public/posts` folder. They won't be displayed in the blog listing until you add details into `public/posts/_data.json`. This is easy-peasy.

## Using different layouts.

This is a bit harder to grasp. You'll have to have a look at `DELETE-AFTER-READING/index.jade`, `another-delete.md` and `DELETE-AFTER-READING/_data.json` to get a sense of what's happening.



