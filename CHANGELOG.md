# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [1.7.6] - 2018-08-21

### Fixed

- Fix bug which leads to wrong key deleted

## [1.7.5] - 2017-12-15

### Fixed

- Fix memory leak in task queue
- Fix python2 on x86 can't convert int to long
- Fix si_unit is not callable
- Fix encoding error with python 2 on windows platform

## [1.7.4] - 2017-10-03

### Changed

- Use larger BUFFER_SIZE for downloads

### Fixed

- Fix bug lead to mkdir conflict in multi threads

## [1.7.3] - 2017-09-28

### Added

- Add SectionReader to replace StringIO

### Changed

- Use 64M for part size
- Fixed read blocksize to 4M

### Fixed

- Improve upload speed on windows platform

## [1.7.2] - 2017-09-20

### Fixed

- Broken dependence on python 2

## [1.7.1] - 2017-09-14

### Added

- Add zone options support
- Add tab completion for linux

### Changed

- Handle illegal characters in a better way
- Modify current_bucket to variable of class

### Fixed

- Fix arg conflict bug
- Fix bug which leads to recursion depth exceeded

## [1.7.0] - 2017-08-11

### Added

- Add support for public bucket
- Add multi thread support for upload and download

### Changed

- Refactor presign command
- Use independent threads to process output
- Use a separate thread to process the progress bar
- Refactor convert_to_bytes function
- Refactor UploadIDRecoder class

## [1.6.2] - 2017-06-20

### Fixed

- Zone should be required while create bucket

## [1.6.1] - 2017-05-23

### Changed

- Use class variable to pass options

### Fixed

- Fix SSL Warnings with old python versions
- Fix part_numbers is not defined error
- Fix bug that cause presign can't work

## [1.6.0] - 2017-05-13

### Added

- Add rate limit feature

### Fixed

- Fix crash when executing the help sub-command

## [1.5.0] - 2017-04-11

### Added

- Add resumimg downloading at break-point
- Add resumimg uploading at break-point
- Handle interrupt signal silently

### Fixed

- Fix duplicate output while detecting config file
- Fix pkg_resource error in python 2.6
- Fix cross-platform coding problems

## [1.4.1] - 2017-03-25

### Fixed

- Fix tqdm encoding error on python 2.6

## [1.4.0] - 2017-03-01

### Added

- Add presign command

### Changed

- Allow user operating buckets granted by policy

### Fixed

- Fix progressbar not close correctly

## [1.3.1] - 2017-02-28

### Fixed

- Fix bug in sync command

## [1.3.0] - 2017-02-27

### Added

- Add progress bar while downloading and uploading

### Changed

- Use DeleteMultipleObjects API instead

### Fixed

- Fix bug while deleting not exist object
- Fix force argument's wrong behavior on multipart
- Fix confirm statement encoding error in python2

## [1.2.3] - 2017-02-08

### Fixed

- Fix bug in using old version config

## [1.2.2] - 2017-01-20

### Changed

- Refactor config file load function, support load config from `~/.qingcloud`
- Be compatible with `qy_access_key_id` and `qy_secret_access_key`

### Fixed

- Fix bug while params is int instead of str

## [1.2.1] - 2017-01-12

### Fixed

- Fix import error in python3

## [1.2.0] - 2017-01-10

### Added

- Support to upload file from stdin

### Fixed

- Fix bug that list_keys do not respect prefix
- Fix empty output while access_key_id is invalid

## [1.1.0] - 2017-01-09

### Changed

- Use [`qingstor-sdk`](https://github.com/yunify/qingstor-sdk-python) instead
- Default config path changed to `~/.qingstor`

### Fixed

- Fix bug when listing buckets under python 3
- Return -1 while download failed

### BREAKING CHANGE

- Config should be updated to new version, older version will be no more supported.

## [1.0.5] - 2016-11-29

### Added

- Catch the exception for file not found

## [1.0.4] - 2016-09-11

### Added

- Add `.gitignore`
- Add MIME Type Detection on File Upload

### Fixed

- Fix bug when printing help pages
- Fix bug when removing empty local directories

## [1.0.3] - 2016-07-26

### Changed

- `PART_SIZE` changed to 32MB
- Validate bucket name before command performs

## 1.0.0 - 2016-07-05

### Added

- Hello, qsctl.

[1.7.6]: https://github.com/yunify/qsctl/compare/1.7.5...1.7.6
[1.7.5]: https://github.com/yunify/qsctl/compare/1.7.4...1.7.5
[1.7.4]: https://github.com/yunify/qsctl/compare/1.7.3...1.7.4
[1.7.3]: https://github.com/yunify/qsctl/compare/1.7.2...1.7.3
[1.7.2]: https://github.com/yunify/qsctl/compare/1.7.1...1.7.2
[1.7.1]: https://github.com/yunify/qsctl/compare/1.7.0...1.7.1
[1.7.0]: https://github.com/yunify/qsctl/compare/1.6.2...1.7.0
[1.6.2]: https://github.com/yunify/qsctl/compare/1.6.1...1.6.2
[1.6.1]: https://github.com/yunify/qsctl/compare/1.6.0...1.6.1
[1.6.0]: https://github.com/yunify/qsctl/compare/1.5.0...1.6.0
[1.5.0]: https://github.com/yunify/qsctl/compare/1.4.1...1.5.0
[1.4.1]: https://github.com/yunify/qsctl/compare/1.4.0...1.4.1
[1.4.0]: https://github.com/yunify/qsctl/compare/1.3.1...1.4.0
[1.3.1]: https://github.com/yunify/qsctl/compare/1.3.0...1.3.1
[1.3.0]: https://github.com/yunify/qsctl/compare/1.2.3...1.3.0
[1.2.3]: https://github.com/yunify/qsctl/compare/1.2.2...1.2.3
[1.2.2]: https://github.com/yunify/qsctl/compare/1.2.1...1.2.2
[1.2.1]: https://github.com/yunify/qsctl/compare/1.2.0...1.2.1
[1.2.0]: https://github.com/yunify/qsctl/compare/1.1.0...1.2.0
[1.1.0]: https://github.com/yunify/qsctl/compare/2cc5fe3c912dc37356d332b103c0f132e1058c63...1.1.0
[1.0.5]: https://github.com/yunify/qsctl/compare/82d42dcaaec9d58c8fdd6cad82bac56092416ff6...2cc5fe3c912dc37356d332b103c0f132e1058c63
[1.0.4]: https://github.com/yunify/qsctl/compare/3073a03e7d2d801226c525e574f9bba295e12ddd...82d42dcaaec9d58c8fdd6cad82bac56092416ff6
[1.0.3]: https://github.com/yunify/qsctl/compare/69a52585edb6b14247e8954722d7b6e680769612...3073a03e7d2d801226c525e574f9bba295e12ddd
