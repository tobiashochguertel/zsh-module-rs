# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2025-11-16

### Changed
- **BREAKING**: Migrated to stable Rust (no longer requires nightly toolchain)
- Removed `trait_alias` feature dependency
- Updated API signatures to use `&CStr` instead of `&str` for better FFI safety
- Renamed `StringArray` to `CStrArray` for clarity
- Renamed `MaybeError` to `MaybeZError` for consistency

### Fixed
- Fixed 7 failing doctests with updated API examples
- Fixed 5 lifetime elision warnings in `zsh/param.rs`
- Added proper imports (`CStr`, `CStrArray`) to documentation examples

### Improved
- All 215 library tests pass
- All 9 doctests now compile successfully (3 intentionally ignored due to macro complexity)
- Clean compilation with zero warnings on stable Rust 1.91.0+

### Documentation
- Updated README with current API examples
- Fixed doctest examples to match current API
- Added explicit lifetime annotations for better clarity

## [0.3.0] - 2023-02-01

### Added
- Initial stable release with high-level ZSH module API
- Support for custom builtin commands
- State management for modules
- ZSH logging functions
- Parameter access

### Known Issues
- Requires nightly Rust due to `trait_alias` feature

## [0.2.1] - 2023-01-XX

- Minor improvements and bug fixes

## [0.2.0] - 2023-01-XX

- API refinements

## [0.1.0] - 2023-01-XX

- Initial release

[0.4.0]: https://github.com/tobiashochguertel/zsh-module-rs/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/tobiashochguertel/zsh-module-rs/compare/v0.2.1...v0.3.0
[0.2.1]: https://github.com/tobiashochguertel/zsh-module-rs/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/tobiashochguertel/zsh-module-rs/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/tobiashochguertel/zsh-module-rs/releases/tag/v0.1.0
