# contributors-from-git

> **Get an array of contributors from a git working tree.**  
> Requires git 1.7+. Forked from `git-contributors` to reduce its scope (no output formatters, command-line interface, sorting or filtering).

[![Build Status][travis_svg]][travis_link] [![Dependency Status][dm_svg]][dm_url]

[travis_svg]: https://travis-ci.org/vweevers/contributors-from-git.svg?branch=master
[travis_link]: https://travis-ci.org/vweevers/contributors-from-git
[dm_svg]: https://david-dm.org/vweevers/contributors-from-git.svg
[dm_url]: https://david-dm.org/vweevers/contributors-from-git

## Usage

```
npm install contributors-from-git
```

```js
var contributors = require('contributors-from-git')

contributors('.', function (err, result) {
  if (err) throw err
  console.log(result)
})
```

This yields an array of contributors:

```js
[
  { commits: 40, name: 'Maja',  email: 'maja@hive' },
  { commits: 10, name: 'Flip',  email: 'flip@meadow' },
  { commits: 80, name: 'Willi', email: 'willi@sunflower' }
]
```

## API

### `contributors(dir, callback)`

The `dir` argument must resolve to a git working tree.

## License

(The MIT License)

Copyright (c) 2014 David Linse <davidlinse@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation
files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
THEWARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
