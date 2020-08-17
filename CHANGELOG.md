# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [2.0.0] - 2020-08-17
### Changed
- renamed `travis` profile to `coveralls`.


## [1.3.1] - 2020-01-22
### Changed
- Same as 1.3.0 release, required additional release due to Maven Central timeouts.

## [1.3.0] - 2020-01-22 [YANKED]
### Yanked
- Timeouts during Maven release resulted in an incomplete deployment to Maven Central.

### Added
- Explicitly add `maven-surefire-plugin` as a build plugin for JUnit5 usage.

## [1.2.0] - 2020-01-10
### Added
- Added [Spotless Maven Plugin](https://github.com/diffplug/spotless/tree/master/plugin-maven), version 1.27.0 with 
  default import order matching most existing Java projects.

## [1.1.0] - 2019-09-03
### Added
- Added `spotbugs-maven-plugin`, version 3.1.12.2.
### Changed
- Updated `eg-oss-plugin-config` version to 1.1.0 (was 1.0.0).
- Updated Jacoco version to 0.8.4 (was 0.8.2) for official Java 11 support.

## [1.0.0] - 2019-07-25
### Changed
- Initial release.
