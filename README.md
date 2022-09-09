# The café website

The complete website of the fictional café. Created according to the graphic design.

<<<<<<< HEAD
## Work in progress

Used technologies:
=======
Technologies and libraries used: Bootstrap 5, Sass, Nunjuck templates, web fonts, Google Maps JS API, npm, Gulp

*Work in progress

# A basic template to develop a website based on Bootstrap 5

Includes:
>>>>>>> main

-   **Bootstrap 5**: build responsive, mobile-first projects on the web with the world's most popular front-end component library
-   **Gulp 4**: task runner for running all of the following
-   **Sass compilation**: leverage the power of the most popular CSS extension language
-   **Sourcemaps** generation for easier Sass debugging
-   **Browsersync**: automatically reloads (or injects in case of CSS), browsers when you change files
-   **Autoprefixer**: parses CSS and adds vendor prefixes according to [caniuse.com]()
-   **UnCSS**: removes unused styles from CSS
-   **CSSO**: CSS minifier with structural optimizations
-   **Nunjucks**: templating language by Mozilla
-   **Surge.sh**: deploy static websites easily and for free

## First time installation

### Install latest [node.js](https://nodejs.org/)

### Install all packages from `package.json` locally

```shell
npm ci
```

_If you’re having errors with `node-gyp`, try [installing it globally](https://github.com/nodejs/node-gyp#installation)._

## Development

To develop with automatic compilation and browser refreshing run

```shell
npm start
```

And see the result on `http://localhost:3000/`

## Build

To build everything once for production deploy (in `/dist/` folder)

This build uses all generated HTML files for _UnCSS_. If it removes something you need to keep, add and array to `ignore` option in `gulpfile.esm.js`.

```shell
npm run build
```

## CSS (Sass preprocessor)

`index.css` is compiled from `src/scss/index.scss` by [Sass](http://sass-lang.com/).

You don't know _Scss_ syntax or don't want to use it? Just use plain CSS in `src/scss/_custom-css.scss`.

## HTML (Nunjucks templates)

HTML is generated from [Nunjucks](https://mozilla.github.io/nunjucks/) templates in `src/templates`.

You don't need to leverage the power of templates. You can just create plain HTML files with `*.njk` extension.

If you don't want a template to be turned into HTML file start it with `_`. Typically these are templates used for _include_ or _extend_.

[Documentation for Nunjucks](https://mozilla.github.io/nunjucks/templating.html).

If you need some data to be available in all templates, use `templates/data.json` for that.

## Static files (JavaScript, images, …)

Folders and files from `/src/static/` are simply copied directly to `/dist/` folder.

### Bootstrap

You can comment out Bootstrap components you don't need in `/src/index.scss`.

`/src/_1-customized-bootstrap-variables.scss` contains only customized Bootstrap variables. Use `/src/_4-customized-bootstrap-variables.scss` instead for your project.

See `browserslist` in `package.json` for supported browsers.

### Deployment

Upload everything in `/dist/` folder to the server.

#### Surge.sh

We use [surge.sh](https://surge.sh) free service for that.

1. If you don’t have a surge account: run surge client with `npx surge` in `/dist` folder to create it.
1. From now on run `npm run deploy` whenever you want to publish a new version.

If you want an acces, contact me.
