# Contributions

## [babel-bridge](https://github.com/CharlesStover/jest/tree/babel-bridge)

Fix babel-core installation instructions ([#6745](https://github.com/facebook/jest/pull/6745))

Documentation was updated to correct dependency listings for Babel transpilation using Babel 7.

Due to Babel 7's lack of backwards compatibility with Babel 6 package names, a "bridge" package was released to point 6 packages to the 7-beta packages.

The bridge package is incorrectly semvar'd in both Babel and Jest documentation, causing the bridge package not to be found by yarn and causing earlier beta builds to match erroneously.

## [it-skip](https://github.com/CharlesStover/jest/tree/it-skip)

Unit testing was updated to correctly mark tests as skipped if the test function is not provided.

Previous behavior throws an error that the test function is a required parameter.

This change more accurately aligns Jest's testing behavior with that of Mocha, resolving [#6430](https://github.com/facebook/jest/issues/6430).
