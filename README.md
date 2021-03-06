# grunt-svninfo

> A Grunt.js plugin that provides easy access to Subversion working copy metadata (svn info).

## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-svninfo --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-svninfo');
```

That's about it, no configuration necessary.

## The "svninfo" task

### Overview
In your project's Gruntfile, add a section named `svninfo` to the data object passed into `grunt.initConfig()`.
Executing the task `svninfo` would run `svn info` in the command line and would make the retrieved data available via grunt.config (e.g. `<%= svninfo.rev %>`) in your build.
The resulting `svninfo` object has the following structure:


```js
{
  "rev": "321",
  "url": "https://yourproject.unfuddle.com/svn/repo/trunk",
  "last": {
 	  "rev": "321",
 	  "author": "me",
 	  "date": "2013-02-10 12:35:30 +0200"
  },
  "repository": {
 	  "root": "https://yourproject.unfuddle.com/svn/repo",
 	  "id": "f5d41312-1fa6-4ca6-a93e-e27d7e98fc43"
  }
}
```

### Options

#### cwd
Type: `String`

Allows to specify a cwd (current working directory) path for the SVN repository of which to retrieve the information. The default directory is the where you run grunt from (`'.'`).

Example:
``` js
svninfo: {
  options: {
    cwd: './myproject/ishere'
  },
  ...
}
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
 * 0.1.2 - Support for 'cwd' option
 * 0.1.1 - Grunt 0.4.x compatibility
 * 0.1.0 - Initial release
