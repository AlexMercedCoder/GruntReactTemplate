# Grunt React Template

A template with grunt.

`npm run build` => concatenates all the js files in source to dist/index.js then babel transpiles and minifies dist/index.js. Keep in mind, concat will concatenate the files in alphabetical order so do consider the naming the of your files.

`npm run dev` => runs build then runs a watcher on which on any change in js files in src which rebuild and start an express server on port 5000. So while the build and server are triggered on save, you still need to refresh the browser to see changes.

- Things to keep in mind, the html has react script tags so there is no need to import or export components

- Zindex.js has this name to ensure it's the last file concatenated, my recommendation is to pre-fix each component file based on component hierarchy.

Z - App
Y - Children of App
X - Grandchildren of App

This will ensure proper concatenation for everything to work
