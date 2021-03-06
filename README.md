fb-node
===============

Slim and simple client for Facebook Graph API v2.* implemented with promises

## Install

```bash
[sudo] npm install fb-node
```

## Usage

```javascript
var api = require('fb-node');

// Set token
api.token = 'Your token';
```

### Methods

api.

- get(url)
- post(url, parameters)
- delete(url)
- put(url, parameters)

All of them returns data that consits from 2 parts: 

- json data
- response object

#### Example

```javascript
api.get('/me').then(function (data) {
  console.log(data.json);
}).catch(function(e){
  console.log(e)
}).finally(function(){
  console.log('Done with the request')
});

api.post('/me/feed', { message: 'Hello, world!' }).then(function (data) {
  console.log(data.json);
}).catch(function(e){
  console.log(e)
}).finally(function(){
  console.log('Done with the request')
});
```

To find URLs and params, go to [Graph API Reference](https://developers.facebook.com/docs/graph-api/reference/v2.1)

### License

```
The MIT License (MIT)

Copyright (c) 2014 Egor Danchenkov

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
