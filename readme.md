*This repository is a mirror of the [component](http://component.io) module [sindresorhus/clone-regexp](http://github.com/sindresorhus/clone-regexp). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/sindresorhus-clone-regexp`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# clone-regexp [![Build Status](https://travis-ci.org/sindresorhus/clone-regexp.svg?branch=master)](https://travis-ci.org/sindresorhus/clone-regexp)

> Clone and modify a [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) instance


## Install

```sh
$ npm install --save clone-regexp
```

```sh
$ bower install --save clone-regexp
```

```sh
$ component install sindresorhus/clone-regexp
```


## Usage

```js
var re = /[a-z]/gi;

cloneRegexp(re);
//=> /[a-z]/gi

cloneRegexp(re) === re;
//=> false

cloneRegexp(re, {global: false});
//=> /[a-z]/i

cloneRegexp(re, {multiline: true});
//=> /[a-z]/gim

cloneRegexp(re, {source: 'unicorn'});
//=> /unicorn/gi
```


## API

### cloneRegexp(regexp, [options])

#### regex

Type: `regexp`

RegExp instance to clone.


#### options

Type: `object`  
Properties: [`source`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/source) [`global`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/global) [`ignoreCase`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/ignoreCase) [`multiline`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) [`sticky`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/sticky) [`unicode`](http://norbertlindenberg.com/2012/05/ecmascript-supplementary-characters/#RegExp)

Optionally modify the cloned RegExp instance.


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
