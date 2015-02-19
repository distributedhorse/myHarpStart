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

To use this, `cd` to the folder where you want to *create* your project and enter the following iin Terminal (after reading the link above) – this will create a folder containing your project so you don't need to `mkdir` anything first:

    sudo npm install -g harp
    harp init your-project-name --boilerplate i41/myHarpStart
    harp server your-project-name -p 9000

Then go to [localhost:9000](http://localhost:9000) and open up the project in your favourite text editor.

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

## Designing in the browser using Harp

I use [LiveReload](http://livereload.com/) to watch the project folder and instantly show changes in the browser. The code to make this happen is already in `_layout.jade`. It looks like this:

        //- delete next line if you're NOT using http://livereload.com/
        <script>document.write('<script src="http://' + (location.host || 'localhost').split(':')[0] + ':35729/livereload.js?snipver=1"></' + 'script>')</script>



