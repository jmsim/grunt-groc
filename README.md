grunt-groc
================

A simple grunt task to generate a project's documentation using Gilt's [Groc](https://github.com/gilt/groc)
(forked from Nevir's [Groc](http://nevir.github.com/groc/)).

Groc depends on [Pygments](http://pygments.org/) to generate documentation. Follow the installation instructions [here](http://pygments.org/docs/installation/).

More capabilities of Gilt's Groc can be found [here](http://tech.gilt.com/post/57089759513/rock-your-doc-with-groc-our-favorite-automated).


### Usage
Install this plugin with the following command:

```js
npm install git+https://github.com/vtjm/grunt-groc.git --save-dev
```

Load the plugin in your Gruntfile.js:

```js
grunt.loadNpmTasks('grunt-groc');
```

Running `grunt groc:javascript` (or `grunt groc` since groc is a multitask) will generate documentation for the specified files.

```js
// Project configuration.
grunt.initConfig({
  groc: {
    javascript: [
      "tasks/*.js", "README.md"
    ],
    options: {
      "out": "doc/"
    }
  }
});
```

See [Groc's cli](http://nevir.github.com/groc/cli.html) for all available options
