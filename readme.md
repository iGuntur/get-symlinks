# get-symlinks [![Build Status](https://travis-ci.org/iguntur/get-symlinks.svg?branch=master)](https://travis-ci.org/iguntur/get-symlinks)

> Get all symbolic link in directory


## Install

```console
$ npm install get-symlinks
```


## Usage

```js
const getSymlinks = require('get-symlinks');

// async
getSymlinks(['/home/guntur/.*']).then(symlinks => {
	console.log(symlinks);
});

// sync
const symlinks = getSymlinks.sync(['/home/guntur/.*', '!/home/guntur/.*rc']);
console.log(symlinks);
```


## API

### getSymlinks(patterns, [options])

Returns a promise for an array of symlinks paths.

### getSymlinks.sync(patterns, [options])

Returns an array of symlinks paths.


#### patterns

- Type: `string`, `array`

    See supported minimatch [patterns](https://github.com/isaacs/minimatch#usage).

    - [Pattern examples with expected matches](https://github.com/sindresorhus/multimatch/blob/master/test.js)
    - [Quick globbing pattern overview](https://github.com/sindresorhus/multimatch#globbing-patterns)


#### options

- Type: `object`

    See the `node-glob` [options](https://github.com/isaacs/node-glob#options).


## Related

- [del-symlinks](https://github.com/iguntur/del-symlinks) - Delete symlinks using glob.
- [is-symbolic-link](https://github.com/iguntur/is-symbolic-link) - Check if PATH is symbolic link


## License

MIT © [Guntur Poetra](https://github.com/iguntur)
