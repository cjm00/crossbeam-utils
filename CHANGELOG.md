# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Fixed
- `CachePadded` supports types bigger than 64 bytes.

### Changed
- Minimum required Rust version is now 1.25.

## [0.3.2] - 2018-03-12
### Fixed
- Mark `load_consume` with `#[inline]`.

## [0.3.1] - 2018-03-12
### Fixed
- `load_consume` on ARM and AArch64.

## [0.3.0] - 2018-03-11
### Added
- `join` for scoped thread API.
- `load_consume` for atomic load-consume memory ordering.

### Removed
- `AtomicOption`.

## [0.2.2] - 2018-01-14
### Added
- Support for Rust 1.12.1.

### Fixed
- Call `T::clone` when cloning a `CachePadded<T>`.

## [0.2.1] - 2017-11-26
### Added
- Add `use_std` feature.

## [0.2.0] - 2017-11-17
### Added
- Add `nightly` feature.
- Use `repr(align(64))` on `CachePadded` with the `nightly` feature.
- Implement `Drop` for `CachePadded<T>`.
- Implement `Clone` for `CachePadded<T>`.
- Implement `From<T>` for `CachePadded<T>`.
- Implement better `Debug` for `CachePadded<T>`.
- Write more tests.
- Add this changelog.

### Changed
- Change cache line length to 64 bytes.

### Removed
- Remove `ZerosValid`.

## 0.1.0 - 2017-08-27
### Added
- Old implementation of `CachePadded` from `crossbeam` version 0.3.0

[Unreleased]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.3.2...HEAD
[0.3.2]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.3.1...v0.3.2
[0.3.1]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.2.2...v0.3.0
[0.2.2]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.2.1...v0.2.2
[0.2.1]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/crossbeam-rs/crossbeam-utils/compare/v0.1.0...v0.2.0
