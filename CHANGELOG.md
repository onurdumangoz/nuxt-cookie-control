# [3.0.0](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.2.4...3.0.0) (2023-01-14)


### Bug Fixes

* **cookie-control:** correct local cloned state configuration usage ([393d59f](https://github.com/dargmuesli/nuxt-cookie-control/commit/393d59f0d077ff5674738336c9046f2c59174c36))
* **cookie-control:** properly save partial cookie configurations ([ebb396e](https://github.com/dargmuesli/nuxt-cookie-control/commit/ebb396ee715ea7dc942ddb001bd4bed39579c9e9))
* **cookie-control:** update local configuration on global change ([8a253eb](https://github.com/dargmuesli/nuxt-cookie-control/commit/8a253ebc8ca9eb39e68f1b164c5d7a2edfef825b))
* **cookie:** set same-site to strict ([0ab00f7](https://github.com/dargmuesli/nuxt-cookie-control/commit/0ab00f7fca5c304e9cc4d747cb0b908c74e7172d))
* **locale:** correct decline string ([f7bce65](https://github.com/dargmuesli/nuxt-cookie-control/commit/f7bce65d90faf7df73cd332843a30dc6459131a1))
* **module:** remove unused Nuxt 2 code ([bd7b234](https://github.com/dargmuesli/nuxt-cookie-control/commit/bd7b234e28037b5f02293074a45b6d53434f9125))
* **playground:** correct locale type ([189e937](https://github.com/dargmuesli/nuxt-cookie-control/commit/189e9378a60df1eebb302fe6c295028f1866b507))
* use js-cookie outside component ([9b689d9](https://github.com/dargmuesli/nuxt-cookie-control/commit/9b689d9ef7742f4ffcc4bdd334b23fa8d751ab14))


* feat!: rework control persistence ([7631391](https://github.com/dargmuesli/nuxt-cookie-control/commit/7631391b8c06dc7bff897aa76814a02a27d5d74f))
* feat(plugin)!: do not initialize cookies ([2d85581](https://github.com/dargmuesli/nuxt-cookie-control/commit/2d85581b3ad4b22ab52257872e046cf9d606a6ef))
* feat!: remove page reload ([9b85dd9](https://github.com/dargmuesli/nuxt-cookie-control/commit/9b85dd985ef6117847e68ee109b237739682b85a))


### Features

* add module option to switch target id visibility ([4264052](https://github.com/dargmuesli/nuxt-cookie-control/commit/42640529820b6e43a2cffcaf8880090db384d44c))


### BREAKING CHANGES

* control persistence is reworked completely, see changes below
- change own cookie names from `(cookie_control_consent, cookie_control_enabled_cookies)` to `(cookie_control_is_consent_given, cookie_control_cookies_enabled_ids)`
- remove methods `useAcceptNecessary`, `acceptNecessary`, `useSetConsent`, `getCookieControlConsent`, `clearCookies`, `setHead`, `setConsent`, `setCookies`
- state properties `cookiesEnabled`, `cookiesEnabledIds` and `isConsentGiven` can be undefined
- include required cookies in enabled cookie list

feat:
- add ability to customize module's own cookie names and expiry
- add method `getCookieIds`

fix:
- correct display of unsaved changes hint
- properly initialize state by reading from cookies
* no cookie is being saved until a user allows cookies to be saved. You now need to check for existence of cookie control's own cookies.
* decide if you need a page reload on cookie configuration change yourself instead! Simply `watch` enabled cookies for changes you wish a page reload for and execute it in your client's code instead of having page reloads forced upon you.

# [3.0.0-beta.7](https://github.com/dargmuesli/nuxt-cookie-control/compare/3.0.0-beta.6...3.0.0-beta.7) (2023-01-14)


### Bug Fixes

* **cookie:** set same-site to strict ([0ab00f7](https://github.com/dargmuesli/nuxt-cookie-control/commit/0ab00f7fca5c304e9cc4d747cb0b908c74e7172d))

# [3.0.0-beta.6](https://github.com/dargmuesli/nuxt-cookie-control/compare/3.0.0-beta.5...3.0.0-beta.6) (2023-01-14)


### Bug Fixes

* use js-cookie outside component ([9b689d9](https://github.com/dargmuesli/nuxt-cookie-control/commit/9b689d9ef7742f4ffcc4bdd334b23fa8d751ab14))

# [3.0.0-beta.5](https://github.com/dargmuesli/nuxt-cookie-control/compare/3.0.0-beta.4...3.0.0-beta.5) (2023-01-14)


### Bug Fixes

* **cookie-control:** properly save partial cookie configurations ([ebb396e](https://github.com/dargmuesli/nuxt-cookie-control/commit/ebb396ee715ea7dc942ddb001bd4bed39579c9e9))

# [3.0.0-beta.4](https://github.com/dargmuesli/nuxt-cookie-control/compare/3.0.0-beta.3...3.0.0-beta.4) (2023-01-14)


### Bug Fixes

* **cookie-control:** update local configuration on global change ([8a253eb](https://github.com/dargmuesli/nuxt-cookie-control/commit/8a253ebc8ca9eb39e68f1b164c5d7a2edfef825b))


### Features

* add module option to switch target id visibility ([4264052](https://github.com/dargmuesli/nuxt-cookie-control/commit/42640529820b6e43a2cffcaf8880090db384d44c))

# [3.0.0-beta.3](https://github.com/dargmuesli/nuxt-cookie-control/compare/3.0.0-beta.2...3.0.0-beta.3) (2023-01-14)


### Bug Fixes

* **cookie-control:** correct local cloned state configuration usage ([393d59f](https://github.com/dargmuesli/nuxt-cookie-control/commit/393d59f0d077ff5674738336c9046f2c59174c36))
* **playground:** correct locale type ([189e937](https://github.com/dargmuesli/nuxt-cookie-control/commit/189e9378a60df1eebb302fe6c295028f1866b507))

# [3.0.0-beta.2](https://github.com/dargmuesli/nuxt-cookie-control/compare/3.0.0-beta.1...3.0.0-beta.2) (2023-01-14)


### Bug Fixes

* **locale:** correct decline string ([f7bce65](https://github.com/dargmuesli/nuxt-cookie-control/commit/f7bce65d90faf7df73cd332843a30dc6459131a1))
* **module:** remove unused Nuxt 2 code ([bd7b234](https://github.com/dargmuesli/nuxt-cookie-control/commit/bd7b234e28037b5f02293074a45b6d53434f9125))


* feat!: rework control persistence ([7631391](https://github.com/dargmuesli/nuxt-cookie-control/commit/7631391b8c06dc7bff897aa76814a02a27d5d74f))
* feat(plugin)!: do not initialize cookies ([2d85581](https://github.com/dargmuesli/nuxt-cookie-control/commit/2d85581b3ad4b22ab52257872e046cf9d606a6ef))


### BREAKING CHANGES

* control persistence is reworked completely, see changes below
- change own cookie names from `(cookie_control_consent, cookie_control_enabled_cookies)` to `(cookie_control_is_consent_given, cookie_control_cookies_enabled_ids)`
- remove methods `useAcceptNecessary`, `acceptNecessary`, `useSetConsent`, `getCookieControlConsent`, `clearCookies`, `setHead`, `setConsent`, `setCookies`
- state properties `cookiesEnabled`, `cookiesEnabledIds` and `isConsentGiven` can be undefined
- include required cookies in enabled cookie list

feat:
- add ability to customize module's own cookie names and expiry
- add method `getCookieIds`

fix:
- correct display of unsaved changes hint
- properly initialize state by reading from cookies
* no cookie is being saved until a user allows cookies to be saved. You now need to check for existence of cookie control's own cookies.

# [3.0.0-beta.1](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.2.4...3.0.0-beta.1) (2023-01-13)


* feat!: remove page reload ([9b85dd9](https://github.com/dargmuesli/nuxt-cookie-control/commit/9b85dd985ef6117847e68ee109b237739682b85a))


### BREAKING CHANGES

* decide if you need a page reload on cookie configuration change yourself instead! Simply `watch` enabled cookies for changes you wish a page reload for and execute it in your client's code instead of having page reloads forced upon you.

## [2.2.4](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.2.3...2.2.4) (2023-01-06)


### Bug Fixes

* **cookie-control:** make color setter toggle more precise ([0477ae8](https://github.com/dargmuesli/nuxt-cookie-control/commit/0477ae8ffbbe5f02ace6ced5e9a51b867cacdefa))

## [2.2.3](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.2.2...2.2.3) (2023-01-06)


### Bug Fixes

* **composables:** set type explicitly ([adfc31e](https://github.com/dargmuesli/nuxt-cookie-control/commit/adfc31eb560e28882c0076ad7a535217660711bf))

## [2.2.2](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.2.1...2.2.2) (2022-12-28)


### Bug Fixes

* **release:** schedule release ([4a3a3e4](https://github.com/dargmuesli/nuxt-cookie-control/commit/4a3a3e4621322afef36a53faec40570afdb54b67))

## [2.2.1](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.2.0...2.2.1) (2022-12-14)


### Bug Fixes

* **component:** make stream function parameter of explicit type ([34e868a](https://github.com/dargmuesli/nuxt-cookie-control/commit/34e868ac9fc25bd689ded6c0292b0376552ef741))

# [2.2.0](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.1.0...2.2.0) (2022-12-14)


### Bug Fixes

* **accept-necessary:** correct setter ([f0881a7](https://github.com/dargmuesli/nuxt-cookie-control/commit/f0881a7d96ace84e37c8ef40a01366d1522581a6)), closes [#13](https://github.com/dargmuesli/nuxt-cookie-control/issues/13)


### Features

* improve modal ux ([b45b9dd](https://github.com/dargmuesli/nuxt-cookie-control/commit/b45b9dd184ec81b75b729326132b14506c1a4f51)), closes [#11](https://github.com/dargmuesli/nuxt-cookie-control/issues/11) [#12](https://github.com/dargmuesli/nuxt-cookie-control/issues/12)

# [2.1.0](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.2...2.1.0) (2022-12-14)


### Bug Fixes

* **de:** correct necessary translation ([c6a200a](https://github.com/dargmuesli/nuxt-cookie-control/commit/c6a200a720c13247b96a9994350f556cdac0d641))


### Features

* **cookie-control:** reorder banner buttons ([130f63a](https://github.com/dargmuesli/nuxt-cookie-control/commit/130f63af7ea29c90bc0f9f817a8f05589692929c))

## [2.0.2](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.1...2.0.2) (2022-12-10)


### Bug Fixes

* **deps:** switch to @sindresorhus/slugify ([99b7dbf](https://github.com/dargmuesli/nuxt-cookie-control/commit/99b7dbfcb47defce2d56f30b96a17f06122cef66))

## [2.0.1](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0...2.0.1) (2022-12-09)


### Bug Fixes

* trigger ci ([6a577a9](https://github.com/dargmuesli/nuxt-cookie-control/commit/6a577a98d09d2591a9a3866188e45041d4717b24))

# [2.0.0](https://github.com/dargmuesli/nuxt-cookie-control/compare/1.9.9...2.0.0) (2022-12-09)


### Bug Fixes

* **component:** extract external dependencies ([31c6945](https://github.com/dargmuesli/nuxt-cookie-control/commit/31c6945b1b53dd638d5050893aa949d08f6fddb4))
* **components:** add missing imports ([aa88808](https://github.com/dargmuesli/nuxt-cookie-control/commit/aa888087086baa7c44298f7d25ddbb073d82893e))
* **components:** add specific types on stream functions ([0fccd65](https://github.com/dargmuesli/nuxt-cookie-control/commit/0fccd65814679892ed85bba86e65ede337d8f85c))
* **components:** correct properties ([ef752ea](https://github.com/dargmuesli/nuxt-cookie-control/commit/ef752ead79150597bac0fba843d86009f3527f80))
* **components:** include typing ([443bda0](https://github.com/dargmuesli/nuxt-cookie-control/commit/443bda0c51fdc0e9abb1c83a33830467f4d27dcb))
* **components:** migrate to script setup ([d7f3b3e](https://github.com/dargmuesli/nuxt-cookie-control/commit/d7f3b3e7ca9d3b30a3c97af2e3ed726297b0f298))
* correct composables ([22faf97](https://github.com/dargmuesli/nuxt-cookie-control/commit/22faf97f2041faaebaecc261d07a87fab89d9511))
* correct typing ([79322a3](https://github.com/dargmuesli/nuxt-cookie-control/commit/79322a38431b23451c305ec960342458b2e13c14))
* correct typing ([bde33f4](https://github.com/dargmuesli/nuxt-cookie-control/commit/bde33f4282d5691cf6be202eeaddc1395047e1bb))
* **eslint:** set end of line to auto ([17890db](https://github.com/dargmuesli/nuxt-cookie-control/commit/17890dbc2f648e49465e26b264337d520d91fe14))
* **git:** ignore output ([a1fa4c3](https://github.com/dargmuesli/nuxt-cookie-control/commit/a1fa4c356e68541ef9872b2ddd42ad147d9512e7))
* **lint-stages:** only lint staged files ([d392cdd](https://github.com/dargmuesli/nuxt-cookie-control/commit/d392cdddc7d4f8afee463352b655307acdc3275f))
* **locale:** correct imports ([71c5eab](https://github.com/dargmuesli/nuxt-cookie-control/commit/71c5eab0a80f7bf9b8e9329d5a4ba4046bb85789))
* **methods:** fallback to default language ([6655207](https://github.com/dargmuesli/nuxt-cookie-control/commit/6655207afebf4e6533902795a2f19f34f0f5c1b9))
* **module:** resolve paths correctly ([b25832c](https://github.com/dargmuesli/nuxt-cookie-control/commit/b25832c53ead00059aedf88fa3b7c0de48f9ec73))
* **package:** add release configuration ([68c944a](https://github.com/dargmuesli/nuxt-cookie-control/commit/68c944ac6c922b95e5bdf848e63e28333dd783d5))
* **package:** correct files ([759c520](https://github.com/dargmuesli/nuxt-cookie-control/commit/759c5205b28ba9fc77370770a0d495a2a6138b0d))
* **package:** correct postinstall hook ([17038d7](https://github.com/dargmuesli/nuxt-cookie-control/commit/17038d7ce6dfff65941fe6bdbffe35317de2bc45))
* **package:** correct scripts ([43d2679](https://github.com/dargmuesli/nuxt-cookie-control/commit/43d2679fbcf128bb644684937882a1d9f1a2a215))
* **package:** correct typecheck command ([3e2fc33](https://github.com/dargmuesli/nuxt-cookie-control/commit/3e2fc33b74c8d02ca5ee0bf19cc848f2ea7b4a89))
* **package:** improve script names ([0d61201](https://github.com/dargmuesli/nuxt-cookie-control/commit/0d6120142ff6645ea073a03e9b969e7d15a4d9df))
* **package:** remove peer dependencies ([7c0efed](https://github.com/dargmuesli/nuxt-cookie-control/commit/7c0efed1e4036b83d0e8ac5aa6755e61900ecb4e))
* **package:** remove release-it ([204394f](https://github.com/dargmuesli/nuxt-cookie-control/commit/204394f92b489c6e3e30b1eef10c34da21bae787))
* **package:** use npm in prepack ([fe73557](https://github.com/dargmuesli/nuxt-cookie-control/commit/fe7355703a094dd0414205a981ab8e3ef816233a))
* **playground:** readd lost nuxt config ([a9dddf8](https://github.com/dargmuesli/nuxt-cookie-control/commit/a9dddf8353c42914680fac2b4e61005fa4482656))
* **runtime:** add imports ([5f5d7c8](https://github.com/dargmuesli/nuxt-cookie-control/commit/5f5d7c85d96f7e5a6175f6b07efda1df287c11c1))
* **src:** add missing tsconfig ([c0a0cd6](https://github.com/dargmuesli/nuxt-cookie-control/commit/c0a0cd651782d0d480e7997878d3562e54d2d2db))


### Features

* add Arabic and Dutch translations ([c0c0422](https://github.com/dargmuesli/nuxt-cookie-control/commit/c0c042279fe60b52f34fe31c6e157ffe0d8c720f))
* begin nuxt 3 migration ([64c997d](https://github.com/dargmuesli/nuxt-cookie-control/commit/64c997d5e7294a066c58036a111034c87621d942))
* continue migration ([a07b462](https://github.com/dargmuesli/nuxt-cookie-control/commit/a07b462f34f0c40da3e4501e5ee178a8f9edf47b))
* continue nuxt 3 migration ([3ace873](https://github.com/dargmuesli/nuxt-cookie-control/commit/3ace873a6566a3a1f06d57794f1bca97a8e066e9))
* **deps:** make peer dependencies optional ([355fd43](https://github.com/dargmuesli/nuxt-cookie-control/commit/355fd439da0630fcda1d75349bdf243cea8732f6))
* finish nuxt 3 migration ([ccc55a7](https://github.com/dargmuesli/nuxt-cookie-control/commit/ccc55a76d7fa2443fbb9cfbe41054751b224f56d))
* import composable ([a07f344](https://github.com/dargmuesli/nuxt-cookie-control/commit/a07f344fdbe6eb9c06c7c267a86912d6688faedd))
* improve typing ([1c982c9](https://github.com/dargmuesli/nuxt-cookie-control/commit/1c982c9f4a95cda91c2be5e89a0ad1b8cf679eb2))
* **playground:** add cookie iframe component ([33f3624](https://github.com/dargmuesli/nuxt-cookie-control/commit/33f3624ee77a07ed1d2193b2ab2cb9d672e18bcc))
* **playground:** add module configuration ([8140d81](https://github.com/dargmuesli/nuxt-cookie-control/commit/8140d8152d68b45edb2939d8934ecc052678af15))
* **plugin:** add nuxt context to accepted / declined calls ([9ac2fd0](https://github.com/dargmuesli/nuxt-cookie-control/commit/9ac2fd03feeae6ec0f316dfafd920b386ca7d9a2))
* **postinstall:** remove outdated link ([0f66469](https://github.com/dargmuesli/nuxt-cookie-control/commit/0f664694f810332db1a7610cbb76917ef83732ef))
* remove `globalname` ([f2d2178](https://github.com/dargmuesli/nuxt-cookie-control/commit/f2d2178f396225096661ed9fe64c9e716bbcc0da))


### BREAKING CHANGES

* `globalname` is not available anymore.

# [2.0.0-beta.7](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0-beta.6...2.0.0-beta.7) (2022-12-09)


### Bug Fixes

* **component:** extract external dependencies ([31c6945](https://github.com/dargmuesli/nuxt-cookie-control/commit/31c6945b1b53dd638d5050893aa949d08f6fddb4))
* **components:** add specific types on stream functions ([0fccd65](https://github.com/dargmuesli/nuxt-cookie-control/commit/0fccd65814679892ed85bba86e65ede337d8f85c))
* **package:** remove peer dependencies ([7c0efed](https://github.com/dargmuesli/nuxt-cookie-control/commit/7c0efed1e4036b83d0e8ac5aa6755e61900ecb4e))

# [2.0.0-beta.6](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0-beta.5...2.0.0-beta.6) (2022-12-08)


### Bug Fixes

* **methods:** fallback to default language ([6655207](https://github.com/dargmuesli/nuxt-cookie-control/commit/6655207afebf4e6533902795a2f19f34f0f5c1b9))

# [2.0.0-beta.5](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0-beta.4...2.0.0-beta.5) (2022-12-08)


### Bug Fixes

* **runtime:** add imports ([5f5d7c8](https://github.com/dargmuesli/nuxt-cookie-control/commit/5f5d7c85d96f7e5a6175f6b07efda1df287c11c1))

# [2.0.0-beta.4](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0-beta.3...2.0.0-beta.4) (2022-12-08)


### Bug Fixes

* **module:** resolve paths correctly ([b25832c](https://github.com/dargmuesli/nuxt-cookie-control/commit/b25832c53ead00059aedf88fa3b7c0de48f9ec73))
* **package:** correct scripts ([43d2679](https://github.com/dargmuesli/nuxt-cookie-control/commit/43d2679fbcf128bb644684937882a1d9f1a2a215))
* **playground:** readd lost nuxt config ([a9dddf8](https://github.com/dargmuesli/nuxt-cookie-control/commit/a9dddf8353c42914680fac2b4e61005fa4482656))

# [2.0.0-beta.3](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0-beta.2...2.0.0-beta.3) (2022-12-08)


### Bug Fixes

* **package:** correct postinstall hook ([17038d7](https://github.com/dargmuesli/nuxt-cookie-control/commit/17038d7ce6dfff65941fe6bdbffe35317de2bc45))

# [2.0.0-beta.2](https://github.com/dargmuesli/nuxt-cookie-control/compare/2.0.0-beta.1...2.0.0-beta.2) (2022-12-08)


### Bug Fixes

* **package:** remove release-it ([204394f](https://github.com/dargmuesli/nuxt-cookie-control/commit/204394f92b489c6e3e30b1eef10c34da21bae787))

# [2.0.0-beta.1](https://github.com/dargmuesli/nuxt-cookie-control/compare/1.9.9...2.0.0-beta.1) (2022-12-08)


### Bug Fixes

* **components:** add missing imports ([aa88808](https://github.com/dargmuesli/nuxt-cookie-control/commit/aa888087086baa7c44298f7d25ddbb073d82893e))
* **components:** correct properties ([ef752ea](https://github.com/dargmuesli/nuxt-cookie-control/commit/ef752ead79150597bac0fba843d86009f3527f80))
* **components:** include typing ([443bda0](https://github.com/dargmuesli/nuxt-cookie-control/commit/443bda0c51fdc0e9abb1c83a33830467f4d27dcb))
* **components:** migrate to script setup ([d7f3b3e](https://github.com/dargmuesli/nuxt-cookie-control/commit/d7f3b3e7ca9d3b30a3c97af2e3ed726297b0f298))
* correct composables ([22faf97](https://github.com/dargmuesli/nuxt-cookie-control/commit/22faf97f2041faaebaecc261d07a87fab89d9511))
* correct typing ([79322a3](https://github.com/dargmuesli/nuxt-cookie-control/commit/79322a38431b23451c305ec960342458b2e13c14))
* correct typing ([bde33f4](https://github.com/dargmuesli/nuxt-cookie-control/commit/bde33f4282d5691cf6be202eeaddc1395047e1bb))
* **eslint:** set end of line to auto ([17890db](https://github.com/dargmuesli/nuxt-cookie-control/commit/17890dbc2f648e49465e26b264337d520d91fe14))
* **git:** ignore output ([a1fa4c3](https://github.com/dargmuesli/nuxt-cookie-control/commit/a1fa4c356e68541ef9872b2ddd42ad147d9512e7))
* **lint-stages:** only lint staged files ([d392cdd](https://github.com/dargmuesli/nuxt-cookie-control/commit/d392cdddc7d4f8afee463352b655307acdc3275f))
* **locale:** correct imports ([71c5eab](https://github.com/dargmuesli/nuxt-cookie-control/commit/71c5eab0a80f7bf9b8e9329d5a4ba4046bb85789))
* **package:** add release configuration ([68c944a](https://github.com/dargmuesli/nuxt-cookie-control/commit/68c944ac6c922b95e5bdf848e63e28333dd783d5))
* **package:** correct files ([759c520](https://github.com/dargmuesli/nuxt-cookie-control/commit/759c5205b28ba9fc77370770a0d495a2a6138b0d))
* **package:** correct typecheck command ([3e2fc33](https://github.com/dargmuesli/nuxt-cookie-control/commit/3e2fc33b74c8d02ca5ee0bf19cc848f2ea7b4a89))
* **package:** improve script names ([0d61201](https://github.com/dargmuesli/nuxt-cookie-control/commit/0d6120142ff6645ea073a03e9b969e7d15a4d9df))
* **package:** use npm in prepack ([fe73557](https://github.com/dargmuesli/nuxt-cookie-control/commit/fe7355703a094dd0414205a981ab8e3ef816233a))
* **src:** add missing tsconfig ([c0a0cd6](https://github.com/dargmuesli/nuxt-cookie-control/commit/c0a0cd651782d0d480e7997878d3562e54d2d2db))


### Features

* add Arabic and Dutch translations ([c0c0422](https://github.com/dargmuesli/nuxt-cookie-control/commit/c0c042279fe60b52f34fe31c6e157ffe0d8c720f))
* begin nuxt 3 migration ([64c997d](https://github.com/dargmuesli/nuxt-cookie-control/commit/64c997d5e7294a066c58036a111034c87621d942))
* continue migration ([a07b462](https://github.com/dargmuesli/nuxt-cookie-control/commit/a07b462f34f0c40da3e4501e5ee178a8f9edf47b))
* continue nuxt 3 migration ([3ace873](https://github.com/dargmuesli/nuxt-cookie-control/commit/3ace873a6566a3a1f06d57794f1bca97a8e066e9))
* **deps:** make peer dependencies optional ([355fd43](https://github.com/dargmuesli/nuxt-cookie-control/commit/355fd439da0630fcda1d75349bdf243cea8732f6))
* finish nuxt 3 migration ([ccc55a7](https://github.com/dargmuesli/nuxt-cookie-control/commit/ccc55a76d7fa2443fbb9cfbe41054751b224f56d))
* import composable ([a07f344](https://github.com/dargmuesli/nuxt-cookie-control/commit/a07f344fdbe6eb9c06c7c267a86912d6688faedd))
* improve typing ([1c982c9](https://github.com/dargmuesli/nuxt-cookie-control/commit/1c982c9f4a95cda91c2be5e89a0ad1b8cf679eb2))
* **playground:** add cookie iframe component ([33f3624](https://github.com/dargmuesli/nuxt-cookie-control/commit/33f3624ee77a07ed1d2193b2ab2cb9d672e18bcc))
* **playground:** add module configuration ([8140d81](https://github.com/dargmuesli/nuxt-cookie-control/commit/8140d8152d68b45edb2939d8934ecc052678af15))
* **plugin:** add nuxt context to accepted / declined calls ([9ac2fd0](https://github.com/dargmuesli/nuxt-cookie-control/commit/9ac2fd03feeae6ec0f316dfafd920b386ca7d9a2))
* **postinstall:** remove outdated link ([0f66469](https://github.com/dargmuesli/nuxt-cookie-control/commit/0f664694f810332db1a7610cbb76917ef83732ef))
* remove `globalname` ([f2d2178](https://github.com/dargmuesli/nuxt-cookie-control/commit/f2d2178f396225096661ed9fe64c9e716bbcc0da))


### BREAKING CHANGES

* `globalname` is not available anymore.
