# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.0] - 2019-02-16
### Added
- Added `--pretty` for converting to Halo Script if a human-readable output is desired

### Changed
- `--strip` is now on by default for if converting to Halo Script

## [2.0.0] - 2019-02-16
### Added
- HSC scripts can now be parsed
- HSC scripts can now be converted into serpent scripts (`parse_hsc_script()` and `compile_serpent_script()`)
- Added `--strip` to make stripping of unnecessary characters optional

### Changed
- Changed the behavior of removing the quotation marks from strings so that only alphanumeric strings (with or without
underscores) have their quotation marks removed rather than strings without spaces.
- Reorganized the file structure. All functions for converting scripts are now stored in a submodule.
- `compile()` is changed to `compile_hsc_script()`
- `parse()` is changed to `parse_serpent_script()`
- Python's `argparse` is used for parsing arguments now

### Fixed
- Empty strings are now properly handled

## [1.3.0] - 2019-02-14
### Added
- Not `!` operator (uses Halo's built-in `not` function)

### Fixed
- `!=` operator was fixed

## [1.2.0] - 2019-02-14
### Changed
- Improved error handling
- File not found errors are properly handled
- CompilerErrors are now actually valid errors

## [1.1.0] - 2019-02-13
### Changed
- Empty globals will now throw an error. They were never compatible with Sapien, and there is no good way to support
them that I can think of.

## [1.0.0] - 2019-02-13
### Added
- Initial release
