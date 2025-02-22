# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [2.6.1] - 2019-10-23

### Added
- Added `--overwrite` option to the `install` command (#3535)

### Changed
- Travis specs now run on node 8 & 10, as opposed to 6 & 8 (#3485)

### Fixed
- Updated octokit/rest to avoid vulnerability (#3602)
- Fixes git package support (#3537)
- Explicit inexact object syntax (#3467)
- Fixes eslint errors in /cli (#3485)

## [2.6.1] - 2019-07-30

### Fixed
- Fix runTests on Windows (#3446)

## [2.6.0] - 2019-07-15

### Added
- Generate stub declarations for subdirectory modules such as `core-js/stable` and `core-js/es/symbol` in core-js (#3426)
- Passing `--typescript` to `create-stub` will use [flowgen](https://github.com/joarwilk/flowgen) to create a stub form an existing, published typescript definition (#3387)

### Removed
- The `version` command has been dropped in favor of the native `--version` flag

## [2.5.2] - 2019-05-15

### Added
- Added `useCacheUntil` flag to `install` command (#3305)

## [2.5.1] - 2018-07-06

### Changed
- Temporarily disable stub guessing (#2485)

## [2.5.0] - 2018-07-06

The flow-typed project has moved to a new organization, [@flow-typed](http://github.com/flow-typed)!

### Added
- Added `cacheDir` flag to `install` and `update` commands (#2016)

### Changed
- Improved stub generation with guessed properties (#2027)
- Replace deprecated `github@0.2.4` with Octokit (#2107)

### Fixed
- Correctly handle uninstalling of scoped packages (#2355)
- Ignore Flow version 0.63.0 when running specs, as it was failing builds (#2423)

## [2.4.0] - 2018-03-16

### IMPORTANT

A week after this release, all previous versions of `flow-typed` on npm will be DEPRECATED, in order to encourage upgrading to version `2.4.0`. After which, we will be introducing files to definition folders under `/definitions/npm`, which will break the `search`, `install` and `validate-defs` commands.

**We strongly recommend upgrading to `2.4.0` within that timeframe.**

### Added
- Allow any file type (.md, .json) under `/definitions/npm/<library>_vx.x.x/` (#1962)
- `describe` and `it` can now be importing from `'flow-typed-test'` in `_test` files (#1942)
  - See [CONTRIBUTING.md](https://github.com/flow-typed/flow-typed/blob/master/CONTRIBUTING.md)
- Root directory option (-rootDir) to install command (#1835)

### Changed
- Replace `unzip` with `unzipper` (#1957)

### Fixed
- Fix jest specs breaking by adding `babel-core` as a dependency (#1864)
