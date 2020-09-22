# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [2.1.0] - TBD
### Changed
- Updated `eg.oss.plugin.config` from 1.1.0 to 1.2.0.
- Updated `failsafe.maven.plugin` from 2.22.0 from to 3.0.0-M5.
- Updated `Jacoco` from 0.8.4 to 0.8.6.
- Updated `checkstyle.plugin` from 3.0.0 to 3.1.1.
- Updated `compiler.plugin` from 3.8.0 to 3.8.1.
- Updated `dependency.plugin` from 3.1.1 to 3.1.2.
- Updated `jar.plugin` from 3.1.0 to 3.2.0.
- Updated `javadoc.plugin` from 3.0.1 to 3.2.0.
- Updated `site.plugin` from 3.7.1 to 3.9.1.
- Updated `source.plugin` from 3.0.1 to 3.2.0.
- Updated `spotbugs.plugin` from 3.1.12.2 to 4.0.4.
- Updated `surefire.plugin` from 2.22.0 to 3.0.0-M5.
- Updated `release.plugin` from 2.5.3 to 3.0.0-M1.
- Updated `spotless.maven.plugin` from 1.27.0 to 2.4.1.


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
