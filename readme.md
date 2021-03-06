# into-stream [![Build Status](https://travis-ci.org/sindresorhus/into-stream.svg?branch=master)](https://travis-ci.org/sindresorhus/into-stream)

> Convert a buffer/string/array/object into a stream

Correctly chunks up the input and handles backpressure.


## Install

```
$ npm install --save into-stream
```


## Usage

```js
const intoStream = require('into-stream');

intoStream('unicorn').pipe(process.stdout);
//=> 'unicorn'
```


## API

### intoStream(input)

Type: `buffer` `string` `array<buffer|string>`<br>
Returns: [Readable stream](https://nodejs.org/api/stream.html#stream_class_stream_readable)

Adheres to the requested chunk size, except for `array` where each element will be a chunk.

### intoStream.obj(input)

Type: `object`, `array<object>`<br>
Returns: [Readable object stream](https://nodejs.org/api/stream.html#stream_object_mode)

## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
