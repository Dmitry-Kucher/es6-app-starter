# ES6 Application Starter project

My version of starter project for JS applications.
Includes [gulp](http://gulpjs.com/) for workflow automation, [babel](https://babeljs.io/) for ES6 syntax transpilation, [eslint](http://eslint.org/) for linter according to [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript).

# Setup

To setting up starter project run following command:
```
npm init
```
It should install all node modules, required for application.

# Project structure

The project includes following directories:
```
/app - public directory for internal webserver
/app/dist - compiled version of all .js files
/src - source files of project
.babelrc, .eslintignore, .editorconfig, .eslintrc, .gitignore - project configuration files
gulpfile.babel.js - gulp tasks description
package.json - required modules description
```

# Gulp Tasks

Gulpfile includes following tasks:
* lint
* lint:fix
* compile
* webserver
* watch
* default

## lint
```
gulp lint
```
Output result will show how many [SLOC](https://en.wikipedia.org/wiki/Source_lines_of_code) had unmatched rules according to linter config

## lint:fix
```
gulp lint:fix
```
Same as previous, but also trying to fix errors if it's possible

## compile
```
gulp compile
```
Put compiled (transpiled) version of js to /app/dist path

## webserver
```
gulp webserver
```
Starting webserver. Be care webserver includes live reloading rule

## watch
```
gulp watch
```
Starting watcher for tracking file changes in /src directory

## default
```
gulp default
```
Starting webserver after linter, compile jobs and keeping watcher for source files. If any changes occured inside /src directory than all process will start again

# Conclusion
Fill free to use any part of code for yor own project and good luck
