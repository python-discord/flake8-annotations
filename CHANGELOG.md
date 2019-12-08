# Changelog
Versions follow [Semantic Versioning](https://semver.org/spec/v2.0.0.html) (`<major>`.`<minor>`.`<patch>`)

## [v1.1.1]
### Added
* Add [`pipenv-setup`](https://github.com/Madoshakalaka/pipenv-setup) as a dev dependency & CI check to ensure synchronization between `Pipfile` and `setup.py`
* Add [tox](https://github.com/tox-dev/tox) configuration for local testing across Python versions
* Add test for checking a single yield of TYP301 per function
* Add coverage reporting to test suite
* Add testing for positional only arguments

### Changed
* [`typed_ast`](https://github.com/python/typed_ast) is now required only for Python versions `< 3.8`
* Update flake8 minimum version to `3.7.9` for Python 3.8 compatibility
* #50 Completely refactor test suite for maintainability

### Fixed
* Fix mixed type hint tests not being run due to misnamed test class
* Fix `TYP301` classification issue where error is not yielded if the first argument is type annotated and the remaining arguments have type comments

## [v1.1.0]
### Added
* #35: Issue templates
* #36: Support for PEP 484-style type comments
* #36: Add `TYP301` for presence of type comment & type annotation for same entity
* #36: Add `error_code.from_function` class method to generate argument for an entire function
* #18: PyPI release via GitHub Action
* #38: Improve `setup.py` metadata

### Fixed
* #32: Incorrect line number for return values in the presence of multiline docstrings
* #33: Improper handling of nested functions in class methods
* `setup.py` dev dependencies out of sync with Pipfile
* Incorrect order of arguments in `Argument` and `Function` `__repr__` methods

## [v1.0.0] - 2019-09-09
Initial release