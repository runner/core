Task runner core
================

[![build status](https://img.shields.io/travis/runner/core.svg?style=flat-square)](https://travis-ci.org/runner/core)
[![npm version](https://img.shields.io/npm/v/@runner/core.svg?style=flat-square)](https://www.npmjs.com/package/@runner/core)
[![dependencies status](https://img.shields.io/david/runner/core.svg?style=flat-square)](https://david-dm.org/runner/core)
[![devDependencies status](https://img.shields.io/david/dev/runner/core.svg?style=flat-square)](https://david-dm.org/runner/core?type=dev)
[![Gitter](https://img.shields.io/badge/gitter-join%20chat-blue.svg?style=flat-square)](https://gitter.im/DarkPark/runner)
[![RunKit](https://img.shields.io/badge/RunKit-try-yellow.svg?style=flat-square)](https://npm.runkit.com/@runner/core)


## Installation ##

```bash
npm install @runner/core
```


## Usage ##

Add to the scope:

```js
var runner = require('@runner/core');
```

Create a simple task:

```js
runner.task('make', function () {
    // some actions
});
```

More examples of tasks creation and execution are available
in the [@cjssdk/runner](https://www.npmjs.com/package/@cjssdk/runner) package.

Add an alias to an existing task:

```js
runner.alias('build', 'make');
```

Run task on a key or keys combination press:

```js
runner.keystroke('build', 'ctrl+b');
```

### Files watching

To execute a specific task on some file changes:

```js
runner.watch('src/script/**/*.js', 'webpack:build');
```

Before calling `runner.watch` it's possible to configure the watch:

```js
runner.watch.config = {
    // some configuration 
};
```

All available configurations you can see in the underlying [chokidar](https://www.npmjs.com/package/chokidar) package.


## Contribution ##

If you have any problems or suggestions please open an [issue](https://github.com/runner/core/issues)
according to the contribution [rules](.github/contributing.md).


## License ##

`@runner/core` is released under the [GPL-3.0 License](http://opensource.org/licenses/GPL-3.0).
