# Change Log

## 1.6.1

### Patch Changes

- [`cdc84d57`](https://github.com/frontity/frontity/commit/cdc84d5700213e579d4fe1a3b586e9d6a5687718) [#335](https://github.com/frontity/frontity/pull/335) Thanks [@luisherranz](https://github.com/luisherranz)! - Fix `isFetching` not turning to true when `data` exists. It may happen in cases where we are fetching that `data` in the embed of others. Like for example, taxonomies in posts.

## 1.6.0

### Minor Changes

- [`e8210ee9`](https://github.com/frontity/frontity/commit/e8210ee97c25555a122dc63f114fb4188ea0b7af) [#253](https://github.com/frontity/frontity/pull/253) Thanks [@michalczaplinski](https://github.com/michalczaplinski)! - We have made easier to work with searches and pagination by adding this new properties to the data object returned by `state.source.get(someLink)`:

  In all entities:

  - `data.link`: the link (short for permalink).
  - `data.page`: the page number.
  - `data.route`: the link without the pagination part.

  In archives:

  - `data.next`: the link of the next page in an archive.
  - `data.previous`: the link of the previous page in an archive.

  In searches:

  - `data.isSearch`: true for links that are searches.
  - `data.searchQuery`: the value of the search.

### Patch Changes

- [`b3225692`](https://github.com/frontity/frontity/commit/b32256929351b66647f64900cc59862ee7c702a7) [#329](https://github.com/frontity/frontity/pull/329) Thanks [@luisherranz](https://github.com/luisherranz)! - Remove `@frontity/connect` from dependencies to avoid multiple imports and fix the problem people is having when they are updating Frontity.
- Updated dependencies [[`b3225692`](https://github.com/frontity/frontity/commit/b32256929351b66647f64900cc59862ee7c702a7), [`e8210ee9`](https://github.com/frontity/frontity/commit/e8210ee97c25555a122dc63f114fb4188ea0b7af), [`b3225692`](https://github.com/frontity/frontity/commit/b32256929351b66647f64900cc59862ee7c702a7), [`f7418071`](https://github.com/frontity/frontity/commit/f741807197c4cda5df2e43f5496a121428d309bf)]:
  - frontity@1.5.2
  - @frontity/source@1.2.0

## 1.5.0

### Minor Changes

- [`fb412d2a`](https://github.com/frontity/frontity/commit/fb412d2af2e9f7cbd5683ea2eb4f961a620edcfc) [#291](https://github.com/frontity/frontity/pull/291) Thanks [@michalczaplinski](https://github.com/michalczaplinski)! - Add status codes and error messages when fetch response is 4xx or 5xx

### Patch Changes

- [`c3d4340a`](https://github.com/frontity/frontity/commit/c3d4340a2ca3088ecda29d2e113d06d8faeb7a0e) [#303](https://github.com/frontity/frontity/pull/303) Thanks [@DAreRodz](https://github.com/DAreRodz)! - Add `force` param to `actions.source.fetch` and `libraries.source.populate`.

  Also, change the default behavior of `populate` to not overwrite entities in the state.- Updated dependencies [[`417f2b0f`](https://github.com/frontity/frontity/commit/417f2b0f0b6f5626be253eb3f1be2daf257b71ef), [`495771f8`](https://github.com/frontity/frontity/commit/495771f83951f192f92d3162221cedc9b791e399), [`696dec11`](https://github.com/frontity/frontity/commit/696dec11bb8d32f0821cca3f5ce39e27c42d60b6), [`80c1aa3a`](https://github.com/frontity/frontity/commit/80c1aa3aee6cf04f46d6fa1a409abfcae2c511cc)]:

  - frontity@1.5.0
  - @frontity/connect@1.0.4

## 1.5.0

### Minor Changes

- [`6ac389b`](https://github.com/frontity/frontity/commit/6ac389b1e406ae32ccb58c7e92c2be84fa4223b8) [#242](https://github.com/frontity/frontity/pull/242) Thanks [@DAreRodz](https://github.com/DAreRodz)! - Add a schema for post types and refactor populate. Use also the new types that come from `@frontity/source`.

### Patch Changes

- Updated dependencies [[`e887fa1`](https://github.com/frontity/frontity/commit/e887fa1d28449cd9189861fe5a4be92fa4acbe33)]:
  - @frontity/source@1.1.0

## [1.4.3](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.4.2...@frontity/wp-source@1.4.3) (2019-12-10)

**Note:** Version bump only for package @frontity/wp-source

## [1.4.2](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.4.1...@frontity/wp-source@1.4.2) (2019-11-04)

### Bug Fixes

- **post-type:** fix handler if a query is present ([0c36a7c](https://github.com/frontity/frontity/commit/0c36a7c))

## [1.4.1](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.4.0...@frontity/wp-source@1.4.1) (2019-10-10)

**Note:** Version bump only for package @frontity/wp-source

# [1.4.0](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.3.1...@frontity/wp-source@1.4.0) (2019-10-02)

### Bug Fixes

- **typescript:** update to latest version ([a89b11c](https://github.com/frontity/frontity/commit/a89b11c))

### Features

- **wp-source:** add postTypes and taxonomies arrays to state ([8f8fce3](https://github.com/frontity/frontity/commit/8f8fce3))

## [1.3.1](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.3.0...@frontity/wp-source@1.3.1) (2019-09-10)

### Bug Fixes

- **wp-source:** move clone-deep from code to tests ([4cd6787](https://github.com/frontity/frontity/commit/4cd6787))

# [1.3.0](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.2.0...@frontity/wp-source@1.3.0) (2019-09-10)

### Bug Fixes

- **wp-source:** allow arrays inside params in api.get ([50fcd63](https://github.com/frontity/frontity/commit/50fcd63))
- **wp-source:** fix handlers, refactor them and improve tests ([#193](https://github.com/frontity/frontity/issues/193)) ([c7e2bfe](https://github.com/frontity/frontity/commit/c7e2bfe))
- **wp-source:** properly populate custom post types and taxonomies ([857f803](https://github.com/frontity/frontity/commit/857f803))

### Features

- **wp-source:** add `postEndpoint` and `params` props to state ([d921b33](https://github.com/frontity/frontity/commit/d921b33))

# [1.2.0](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.8...@frontity/wp-source@1.2.0) (2019-08-12)

### Bug Fixes

- **wp-source:** do not set `isHome` in `postArchive` handler ([#179](https://github.com/frontity/frontity/issues/179)) ([13e5c1e](https://github.com/frontity/frontity/commit/13e5c1e))

### Features

- **frontity:** expose fetch and URL from frontity package ([#168](https://github.com/frontity/frontity/issues/168)) ([235c465](https://github.com/frontity/frontity/commit/235c465))

## [1.1.8](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.7...@frontity/wp-source@1.1.8) (2019-07-12)

### Bug Fixes

- **source:** set isHome value for the home data object ([9af88b4](https://github.com/frontity/frontity/commit/9af88b4))

## [1.1.7](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.6...@frontity/wp-source@1.1.7) (2019-07-04)

**Note:** Version bump only for package @frontity/wp-source

## [1.1.6](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.5...@frontity/wp-source@1.1.6) (2019-07-04)

### Bug Fixes

- **babel:** use workaround for a bug in babel 7.5.0 ([3c489ae](https://github.com/frontity/frontity/commit/3c489ae))

## [1.1.5](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.4...@frontity/wp-source@1.1.5) (2019-07-01)

**Note:** Version bump only for package @frontity/wp-source

## [1.1.4](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.3...@frontity/wp-source@1.1.4) (2019-06-20)

**Note:** Version bump only for package @frontity/wp-source

## [1.1.3](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.2...@frontity/wp-source@1.1.3) (2019-06-20)

**Note:** Version bump only for package @frontity/wp-source

## [1.1.2](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.1...@frontity/wp-source@1.1.2) (2019-06-20)

**Note:** Version bump only for package @frontity/wp-source

## [1.1.1](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.1.0...@frontity/wp-source@1.1.1) (2019-06-19)

**Note:** Version bump only for package @frontity/wp-source

# [1.1.0](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.0.3...@frontity/wp-source@1.1.0) (2019-06-19)

### Features

- **wp-source:** add support for subdirectory, redirections, pages as home, category and tag base ([#131](https://github.com/frontity/frontity/issues/131)) ([0b877b2](https://github.com/frontity/frontity/commit/0b877b2))

## [1.0.3](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.0.2...@frontity/wp-source@1.0.3) (2019-06-19)

### Bug Fixes

- **source-get:** make isFetching and isReady properties to be always present ([#122](https://github.com/frontity/frontity/issues/122)) ([6d2e485](https://github.com/frontity/frontity/commit/6d2e485))

## [1.0.2](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.0.1...@frontity/wp-source@1.0.2) (2019-06-05)

### Bug Fixes

- **source:** fix wrong import in source tests ([209cdfd](https://github.com/frontity/frontity/commit/209cdfd))

## [1.0.1](https://github.com/frontity/frontity/compare/@frontity/wp-source@1.0.0...@frontity/wp-source@1.0.1) (2019-06-05)

### Bug Fixes

- **all:** update typscript and fix some keywords ([1fe5fec](https://github.com/frontity/frontity/commit/1fe5fec))
- **wp-source:** change apiUrl for api ([26947e7](https://github.com/frontity/frontity/commit/26947e7))

# [1.0.0](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.7...@frontity/wp-source@1.0.0) (2019-06-05)

### Bug Fixes

- **route-utils:** support custom names in routes ([1b0994b](https://github.com/frontity/frontity/commit/1b0994b))
- **source:** change routeUtils functions to "getParams" and "getRoute" ([e385d3c](https://github.com/frontity/frontity/commit/e385d3c))
- **wp-source:** fix archive handlers ([c09736f](https://github.com/frontity/frontity/commit/c09736f))
- **wp-source:** fix searches in taxonomies ([8b9257f](https://github.com/frontity/frontity/commit/8b9257f))
- **wp-source:** remove domains from links ([f111b8c](https://github.com/frontity/frontity/commit/f111b8c))
- **wp-source:** transform WpSource into a function ([abd7034](https://github.com/frontity/frontity/commit/abd7034))

### Features

- **source:** accept only strings in 'source.get' and 'source.fetch' ([2e9ae62](https://github.com/frontity/frontity/commit/2e9ae62))
- **source:** add 'normalize' to libraries ([9e0e9e3](https://github.com/frontity/frontity/commit/9e0e9e3))
- **source:** change 'data' to 'get' and 'dataMap' to 'data' ([f32be1a](https://github.com/frontity/frontity/commit/f32be1a))
- **source:** move list pages to their own data ([148bc0a](https://github.com/frontity/frontity/commit/148bc0a))
- **source:** rename route libraries to 'stringify' and 'parse' ([f230f86](https://github.com/frontity/frontity/commit/f230f86))
- **wp-source:** add library 'routeUtils' ([0a31246](https://github.com/frontity/frontity/commit/0a31246))
- **wp-source:** remove domain from links ([ff1752b](https://github.com/frontity/frontity/commit/ff1752b))

### BREAKING CHANGES

- **source:** objects cannot be passed as arguments in 'source.get' and 'source.set'
- **source:** route libraries have new names
- **source:** "data.pages" doesn't exist anymore, use "data.items" instead. Each "route" represents now an archive's page (if "route" points to an archive).
- **source:** changes source API ("data" by "get")

## [0.1.7](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.6...@frontity/wp-source@0.1.7) (2019-05-20)

**Note:** Version bump only for package @frontity/wp-source

## [0.1.6](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.5...@frontity/wp-source@0.1.6) (2019-05-17)

**Note:** Version bump only for package @frontity/wp-source

## [0.1.5](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.4...@frontity/wp-source@0.1.5) (2019-05-16)

**Note:** Version bump only for package @frontity/wp-source

## [0.1.4](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.3...@frontity/wp-source@0.1.4) (2019-05-16)

**Note:** Version bump only for package @frontity/wp-source

## [0.1.3](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.2...@frontity/wp-source@0.1.3) (2019-05-15)

**Note:** Version bump only for package @frontity/wp-source

## [0.1.2](https://github.com/frontity/frontity/compare/@frontity/wp-source@0.1.1...@frontity/wp-source@0.1.2) (2019-05-15)

**Note:** Version bump only for package @frontity/wp-source

## 0.1.1 (2019-05-15)

### Bug Fixes

- **jest-config:** transform js files with ts-jest ([943b3e4](https://github.com/frontity/frontity/commit/943b3e4))
