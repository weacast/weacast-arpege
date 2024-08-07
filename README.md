> **Important:** this module is now deprecated, please use the corresponding package in the [weacast monorepo](https://github.com/weacast/weacast).

# weacast-arpege

[![Build Status](https://app.travis-ci.com/weacast/weacast-arpege.svg?branch=master)](https://app.travis-ci.com/weacast/weacast-arpege)
[![Code Climate](https://codeclimate.com/github/weacast/weacast-arpege/badges/gpa.svg)](https://codeclimate.com/github/weacast/weacast-arpege)
[![Test Coverage](https://codeclimate.com/github/weacast/weacast-arpege/badges/coverage.svg)](https://codeclimate.com/github/weacast/weacast-arpege/coverage)
[![Dependency Status](https://img.shields.io/david/weacast/weacast-arpege.svg?style=flat-square)](https://david-dm.org/weacast/weacast-arpege)
[![Documentation](https://img.shields.io/badge/documentation-available-brightgreen.svg)](https://weacast.github.io/weacast-docs/)
[![Download Status](https://img.shields.io/npm/dm/weacast-arpege.svg?style=flat-square)](https://www.npmjs.com/package/weacast-arpege)

> ARPEGE weather forecast model plugin for Weacast

## Installation

```
npm install weacast-arpege --save
// Or with Yarn
yarn add weacast-arpege
```

## Documentation

The [Weacast docs](https://weacast.github.io/weacast-docs/) are loaded with awesome stuff and tell you everything you need to know about using and configuring Weacast. Some details about this plugin can be found [here](https://weacast.gitbooks.io/weacast-docs/api/PLUGIN.html#arpege).

## Complete Example

Here's an example of a Weacast server that uses `weacast-arpege`. 

```js
import arpegePlugin from 'weacast-arpege'

module.exports = function() {
  const app = this
  
  // Set up our plugin services
  app.configure(arpegePlugin)
}
```
## Development

While it is a WIP and not yet pushed to NPM, or when developing this plugin, please clone this repository and use [npm link](https://docs.npmjs.com/cli/link):

```bash
// Clone and link the plugin
git clone https://github.com/weacast/weacast-arpege.git
cd weacast-arpege
npm link
// Clone and link plugin to weacast server
cd ..
git clone https://github.com/weacast/weacast.git
cd weacast
cd api
npm link weacast-arpege
```

As this module also depends on [weacast-core](https://github.com/weacast/weacast-core) and [gtiff2json](https://github.com/weacast/gtiff2json) you have to do the same thing for them.

## License

Copyright (c) 2017

Licensed under the [MIT license](LICENSE).
