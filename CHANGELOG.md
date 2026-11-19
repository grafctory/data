# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres
to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased](https://github.com/metreeca/pipe/compare/v0.13.0...HEAD)

## [0.13.0](https://github.com/metreeca/pipe/compare/v0.12.0...v0.13.0) - 2026-11-19

### Changed

- **Breaking**: Upgrade `@metreeca/gear` to `^0.6.0`; projects using it alongside these packages raise their own range
  to match as well, so that the executor they start and the services the tasks resolve come from a single copy

- **Breaking**: `@metreeca/pipe-sparql`, `@metreeca/pipe-store` and `@metreeca/pipe-url` take `@metreeca/gear` as a
  peer dependency, so that an app installs a single copy of it and every task resolves the services bound to the
  execution the app starts; apps declare `@metreeca/gear` among their own dependencies to run the executor

## [0.12.0](https://github.com/metreeca/pipe/compare/v0.11.1...v0.12.0) - 2026-11-17

### Changed

- **Breaking**: Upgrade `@metreeca/blue` to `^0.14.0`, `@metreeca/core` to `^0.14.0`, `@metreeca/flow` to `^0.13.0`,
  `@metreeca/gear` to `^0.5.0`, `@metreeca/http` to `^0.6.0`, `@metreeca/keep` to `^0.13.0`, `@metreeca/qest` to
  `^0.14.0`, `@metreeca/tape` to `^0.13.0`, `@metreeca/trio` to `^0.3.0` and `@metreeca/wire-sparql` to `^0.13.0`;
  projects using them alongside these packages raise their own ranges as well, so that each is shared as a single copy
- **Breaking**: `@metreeca/pipe-url` `fetch()` no longer rejects when an exchange fails without a response, such as on
  a timeout or a refused connection: the failure is logged and the request dropped, as an unsuccessful status already
  was, so the feed runs to completion; jobs that relied on the rejection to stop check the log for failed exchanges

### Security

- Upgrade the `vite`, `vitest` and `markdown-it` development dependencies to `8.3.5`, `4.1.12` and `14.3.3`
  respectively (GHSA-587h-7wmj-h5pm, GHSA-698v-4r3x-3vcv, GHSA-r825-w8mm-5pxw, GHSA-vfpm-58rq-9qcg,
  GHSA-rq7h-c2jc-7f22, GHSA-9jrq-w75r-8gcw, GHSA-qxg6-89mg-rqv8, GHSA-xp26-3454-mjgp, GHSA-gfr2-rv44-r23c,
  GHSA-r7fv-28h4-cvq7, GHSA-vfgh-jcmw-g37q); the published packages are unaffected

## [0.11.1](https://github.com/metreeca/pipe/compare/v0.11.0...v0.11.1) - 2026-10-20

### Fixed

- Publish `@metreeca/pipe-url` with the `0.11.0` content, which the registry refused under that version

## [0.11.0](https://github.com/metreeca/pipe/compare/v0.10.1...v0.11.0) - 2026-10-20

### Added

- `@metreeca/pipe-sparql` package with `select`, `construct`, `update` and `upload` steps for SPARQL endpoints
- `@metreeca/pipe-store` package with `lookup`, `retire` and `settle` steps for `@metreeca/keep` stores

### Changed

- Upgrade `@metreeca/core` to `^0.13.0`
- Upgrade `@metreeca/flow` to `^0.12.0`
- Upgrade `@metreeca/gear` to `^0.4.0`
- Upgrade `@metreeca/http` to `^0.5.0`
- Upgrade `@metreeca/tape` to `^0.12.0`

## [0.10.1](https://github.com/metreeca/pipe/compare/v0.10.0...v0.10.1) - 2026-10-14

### Changed

- Upgrade `@metreeca/core` to `^0.12.1`
- Upgrade `@metreeca/flow` to `^0.11.1`
- Upgrade `@metreeca/gear` to `^0.3.1`
- Upgrade `@metreeca/http` to `^0.4.1`
- Upgrade `@metreeca/tape` to `^0.11.1`

## [0.10.0](https://github.com/metreeca/pipe/releases/tag/v0.10.0) - 2026-10-01

Initial release of the source family task packages, running under the `@metreeca/gear` job executor.

- `@metreeca/pipe-url` — URL processing tasks, formerly `@metreeca/gear-url`
