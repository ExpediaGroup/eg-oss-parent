# eg-oss-parent

## Start using

You can obtain this POM from Maven Central:

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.expediagroup/eg-oss-parent/badge.svg?subject=com.expediagroup:eg-oss-parent.pom)](https://maven-badges.herokuapp.com/maven-central/com.expediagroup/eg-oss-parent) [![Build Status](https://travis-ci.org/ExpediaGroup/eg-oss-parent.svg?branch=master)](https://travis-ci.org/ExpediaGroup/eg-oss-parent) ![GitHub license](https://img.shields.io/github/license/ExpediaGroup/eg-oss-parent.svg)

## Overview
The Expedia Group OSS Parent POM provides a Maven parent POM that is intended to be used by Expedia Group projects that require certain 
base functionality and need to publish artifacts to [Maven Central](https://search.maven.org/).

# Plugins
## [Jib Maven plugin](https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin)
This plugin builds an optimized Docker image for a Java application and uploads it to [Docker Hub](https://hub.docker.com/).

To setup the plugin in a child project add the following plugin references. The `git-commit-id-plugin` provides the 
last commit time to be used for the `creationTime` and `filesModificationTime` properties in the jib plugin configuration.
```xml
<plugin>
    <groupId>com.google.cloud.tools</groupId>
    <artifactId>jib-maven-plugin</artifactId>
</plugin>
<plugin>
    <groupId>pl.project13.maven</groupId>
    <artifactId>git-commit-id-plugin</artifactId>
</plugin>
```

# Legal
This project is available under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0.html).

Copyright 2019-2021 Expedia, Inc.
