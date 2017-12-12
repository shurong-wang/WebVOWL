WebVOWL [![Build Status](https://travis-ci.org/VisualDataWeb/WebVOWL.svg?branch=master)](https://travis-ci.org/VisualDataWeb/WebVOWL)
=======

This repository was ported from an internal SVN repository to Github after the release of WebVOWL 0.4.0. Due to cleanups with `git filter-branch`, the commit history might show some strange effects.


Requirements
------------

Node.js for installing the development tools and dependencies.
Development setup
-----------------

### Simple ###
1. Download and install Node.js from http://nodejs.org/download/
2. Open the terminal in the root directory
3. Run `npm install` to install the dependencies and build the project
4. Edit the code
5. Run `npm run-script release` to (re-)build all necessary files into the deploy directory

### Advanced ###
Instead of the last step of the simple setup, install the npm package `grunt-cli` globally with
`npm install grunt-cli -g`. Now you can execute a few more advanced commands in the terminal:

* `grunt` or `grunt release` builds the release files into the deploy directory
* `grunt package` builds the development version
* `grunt webserver` starts a local live-updating webserver with the current development version
* `grunt test` starts the test runner
* `grunt zip` builds the project and puts it into a zip file


Additional information
----------------------

To export the VOWL visualization to an SVG image, all css styles have to be included into the SVG code.
This means that if you change the CSS code in the `vowl.css` file, you also have to update the code that
inlines the styles - otherwise the exported SVG will not look the same as the displayed graph.

The tool which creates the code that inlines the styles can be found in the util directory. Please
follow the instructions:

# VOWLCSSToD3RuleConverter

This tool converts all rules from the `vowl.css` file into javascript code that can be executed to
inline the styles. This is required because otherwise the exported SVG files won't have any styles.

This should be integrated into the build process so it won't be overlooked.


## How to run

1. Run `npm install` in the root directory of this project to install the dependency which
processes the css code.
2. Run it with `node code.js` to receive the javascript code which can inline and remove the styles.
3. Insert the two code blocks into the matching functions in the `exportMenu.js` file.