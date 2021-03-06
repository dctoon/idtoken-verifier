# Change Log

## [v1.0.1](https://github.com/auth0/auth0.js/tree/v1.0.1) (2017-05-08)
[Full Changelog](https://github.com/auth0/auth0.js/compare/v1.0.0...v1.0.1)

**Fixed**
- Handle JSON.parse errors during decode [\#3](https://github.com/auth0/idtoken-verifier/pull/3) ([rolodato](https://github.com/rolodato))

## [v1.0.0](https://github.com/auth0/idtoken-verifier/tree/v1.0.0) (2016-12-30)
[Full Changelog](https://github.com/auth0/idtoken-verifier/tree/v1.0.0)

A lightweight library to decode and verify RS JWT meant for the browser.

### Usage

```js
var IdTokenVerifier = require('idtoken-verifier');

var verifier = new IdTokenVerifier({
        issuer: 'https://my.auth0.com/',
        audience: 'gYSNlU4YC4V1YPdqq8zPQcup6rJw1Mbt'
    });

verifier.verify(id_token, nonce, function(error, payload) {
    ...
});

var decoded = verifier.decode(id_token);
```