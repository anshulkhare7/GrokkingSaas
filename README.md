[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Installing SASS Locally

Before we can write Sass code, it needs to be installed locally. As by default, it’s not a language known to the browser.

Let’s now go through the process to setup the environment that will allow us to write then compile Sass.

>>Note: When Sass is compiled, it is converted into regular CSS code that browsers can interpret and render.

### Environment setup

You must have *npm* installed on your computer, it comes bundled with *Node.js*.

### Folder Structure

Let’s create our project folders! They will be structured like so:

sass-project
   |- sass/main.scss
   |- css/style.css
   |- index.html

### Initializing our Project Directory

All projects that use npm need to be initialized. From inside the sass-project folder, run the following command:

`$npm init -y`

This will create a package.json file for our project.

### Install node-sass

*node-sass* is the library which allows us to compile .scss to .css.

Install node-sass as dev dependency.

`$npm install node-sass --save-dev`

>>Note: A dev dependency is only used in the build phase of our project. It’s not included at runtime.

### Compiling Sass Code to CSS

We need to create an npm script to run the compilation.

Add this script inside the script section of our previously created package.json file:

>>"compile-sass": "node-sass sass/main.scss css/style.css"

Don’t forget to separate each script with a comma!

We have here specified main.scss as our main Sass file and style.css as the compiled CSS file.

To compile our SASS code into CSS, all we need to do is run:

`$npm run compile-sass`

### Live Reload

Let’s also add a live reload to our project! To do this run the following to install globally:

`$npm install live-server -g`

Now, make sure you’re still in the Sass project folder, and run:

`$live-server`

Now, you’ve got a dev environment with your project running locally on HTTP.

You’ll need to keep live-server and npm run compile-sass running in two separate terminal windows.

So we now have the project environment all set up on the local machine!

`$npm install concat --save-dev`

`$npm install autoprefixer --save-dev`

`$npm install postcss-cli --save-dev`

`$npm install npm-run-all --save-dev`
