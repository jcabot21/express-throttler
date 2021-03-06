# Express-Simple-Throttler

[![npm version](https://badge.fury.io/js/express-simple-throttler.svg)](https://badge.fury.io/js/express-simple-throttler)
[![CircleCI](https://circleci.com/gh/jcabot21/express-simple-throttler.svg?style=shield)](https://circleci.com/gh/jcabot21/express-throttler)
[![Coverage Status](https://coveralls.io/repos/github/jcabot21/express-throttler/badge.svg?branch=master)](https://coveralls.io/github/jcabot21/express-throttler?branch=develop)

Super tiny helper middleware for slowing down requests. Use for your testing.

## Install

`npm install express-simple-throttler`

## How-to

The middleware comes in two flavors, constant and random.

### Constant

```js
const throttler = require('express-throttler');
const app = require('express')();
const twentySeconds = 20 * 1000;

app.use(throttler(twentySeconds));

// Setup your routes, now they are all super slow
// ...
```

### Random

```js
const throttler = require('express-throttler');
const app = require('express')();
const upToTwentySeconds = 20 * 1000;

app.use(throttler(upToTwentySeconds, true));

// Setup your routes, now some may be super slow
// ...
```

## Tests

Tests are run with jasmine through the test command as follows:

`npm test`
