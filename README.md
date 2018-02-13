# http-shortcut

`http-shortcut` is a simple node.js library for small http requests.

# Example

```javascript
const { httpRequestF } = require('http-shortcut');

const requestOptions = {
    protocol: 'https:',
    hostname: 'api.example.com',
    port: 443,
    method: 'POST',
    path: `/v1/events`,
};

const evt = {
    foo: 'bar',
};

httpRequestF(requestOptions, JSON.stringify(evt))
    .then(res => res.checkResponse());
```
