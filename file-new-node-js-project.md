File New Node.js Project
===

Steps to create a new Node.js console app.

Setup a Git Repository
---
If you require a git repo to keep all of your work:

 - create on github
 -  `git clone repo@repo`
 - stick a .gitignore file in the dir as well if not exist


Initialise the Node.js app
---
 - move to the directory containing the git repo
 - `npm init` which makes packages.json
 - edit packages.json make sure "main" points to a real js file that you will need to create
 - put a `console.log()` into the main js file
 - test everything is working by running `node .`


Setup Jasmine Unit Testing
---
 - `npm install jasmine --save-dev`
 - `jasmine init`
  - this should update packages.json and create spec folder
  - if jasmine command not recognised then `npm install -g jasmine`
 - create any *spec.js file in spec folder with `console.log()` inside an `it()` block 
 - test jasmine is working by running `jasmine` and observing the `console.log()` output


Arrange setup with appropriate files:
---

main.js:

    var module_name = require("./module_name");
    module_name.run();


module_name.js:

    exports.run = function() {
    	// runs
    };


module_name-tests.spec.js:

    var module_name = require("../module_name");
    // tests
