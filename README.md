# mi9-web-service [![Build Status](https://travis-ci.org/harvest316/mi9-web-service.png?branch=master)](https://travis-ci.org/harvest316/mi9-web-service)

This successful submission to the Mi9 Web Service Coding Challenge filters a given [JSON list of TV shows](https://github.com/mi9/coding-challenge-samples/blob/master/sample_response.json), returning the subset of these shows that have DRM enabled and at least one episode.

By [Paul Harvey](http://paulharvey.com.au) (harvest316)

## Installation

Download node at [nodejs.org](http://nodejs.org) and install it, if you haven't already.

```sh
npm install mi9-web-service --save
```


## Tests

```sh
npm install
npm test
```
```

    The sample request provided by Mi9 contains both wanted and unwanted shows
    The sample response provided by Mi9 contains only the wanted shows
    Wanted shows are DRM enabled with at least one episode

  The Mi9 Web Service:
    √ Should Return Mi9 Sample Response Given Mi9 Sample Request
    √ Should Return Only Wanted Shows Given Only Wanted Shows
    √ Should Return 400 Parse Error Given Skip + Take > TotalRecords
    √ Should Return Single Show Given Single Wanted Show
    √ Should Return Empty Response Given Single Unwanted Show
    √ Should Return Empty Response Given Only Zero-Episode Shows
    √ Should Return Empty Response Given Only Non-DRM Shows
    √ Should Return 404 Not Found Given Unknown Path
    √ Should Return 400 Parse Error Given Missing Request
    √ Should Return 400 Parse Error Given Null Request
    √ Should Return 400 Parse Error Given Empty JSON Request
    √ Should Return 400 Parse Error Given Empty String Request
    √ Should Return 400 Parse Error Given Empty Payload
    √ Should Return 400 Parse Error Given Invalid Schema
    √ Should Return 400 Parse Error Given Invalid MIME Type
    √ Should Return 400 Parse Error Given Non-JSON Request
    - Should Return Wanted Shows 1..4 Given Mi9 Sample Request And Skip Is 0 And Take Is 4
    - Should Return Wanted Shows 5..7 Given Mi9 Sample Request And Skip Is 4 And Take Is 4
  The Test Data:
    √ sampleRequest Should Return 10 Records
    √ sampleResponse Should Return 7 Records
    √ emptyResponse Should Return 0 Records
    √ requestWithEmptyPayload Should Return Valid Fields
    √ requestWithJustOneShow Should Return 1 Record
    √ requestWithOnlyNonDRMShows Should Return 2 Records
    √ requestWithOnlyZeroEpisodeShows Should Return 3 Records
    √ requestWithOnlyValidShows Should Return 7 Records
  
```

## Dependencies

- [async](https://github.com/caolan/async): Higher-order functions and common patterns for asynchronous code
- [body-parser](https://github.com/expressjs/body-parser): Node.js body parsing middleware
- [express](https://github.com/strongloop/express): Fast, unopinionated, minimalist web framework
- [underscore](https://github.com/jashkenas/underscore): JavaScript&#39;s functional programming helper library.
- [winston](https://github.com/flatiron/winston): A multi-transport async logging library for Node.js

## Dev Dependencies

- [chai](https://github.com/chaijs/chai): BDD/TDD assertion library for node.js and the browser. Test framework agnostic.
- [chai-json-schema](https://github.com/Bartvds/chai-json-schema): Chai plugin for JSON Schema v4
- [debug](https://github.com/visionmedia/debug): small debugging utility
- [dotenv](https://github.com/motdotla/dotenv): Loads environment variables from .env file
- [expect.js](https://github.com/LearnBoost/expect.js): BDD style assertions for node and the browser.
- [grunt](https://github.com/gruntjs/grunt): The JavaScript Task Runner
- [grunt-contrib-jshint](https://github.com/gruntjs/grunt-contrib-jshint): Validate files with JSHint.
- [grunt-jsdoc](https://github.com/krampstudio/grunt-jsdoc): Integrates jsdoc3 generation into your Grunt build
- [grunt-simple-mocha](https://github.com/yaymukund/grunt-simple-mocha): A simple wrapper for running tests with Mocha.
- [jsdoc](https://github.com/jsdoc3/jsdoc): An API documentation generator for JavaScript.
- [mocha](https://github.com/visionmedia/mocha): simple, flexible, fun test framework
- [superagent](https://github.com/visionmedia/superagent): elegant &amp; feature rich browser / node HTTP with a fluent API


## License

MIT

_Generated by [package-json-to-readme](https://github.com/zeke/package-json-to-readme)_
