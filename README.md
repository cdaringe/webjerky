# webjerky

connect to sauce, fire up a static server, do some screenshot testing!

webjerky is a tiny script that wires together a few webjerk plugins, & runs element-wise screenshot testing in saucelabs.  you can read the single file source for a better idea!

## usage

```js
var webjerky = require('webjerky)
/**
 * @module webjerky
 * @param {object} conf
 * @param {string} conf.testName
 * @param {string} conf.staticDir
 * @param {string} [conf.sauceUsername] defaults to process.env.SAUCE_USERNAME
 * @param {string} [conf.sauceAccessKey] defaults to process.env.SAUCE_ACCESS_KEY
 * @param {object} conf.snapDefinitions see webjerk-snaps for more
 * @param {function} [conf.snapDefinitionsFromWindow] can be used instead of snap snapDefinitions. see webjerk-snaps for more
 * @returns {Promise}
 */
var conf = { ... }
webjerky(conf).then(...) // `snaps/` will be a dir with the result of `webjerk-snaps` within!
```
