# eg-oss-parent


## Start using

You can obtain this POM from Maven Central:

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.expediagroup/eg-oss-parent/badge.svg?subject=com.expediagroup:eg-oss-parent.pom)](https://maven-badges.herokuapp.com/maven-central/com.expediagroup/eg-oss-parent) [![Build Status](https://travis-ci.org/ExpediaGroup/eg-oss-parent.svg?branch=main)](https://travis-ci.org/ExpediaGroup/eg-oss-parent) ![GitHub license](https://img.shields.io/github/license/ExpediaGroup/eg-oss-parent.svg)

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

There are some default configuration properties that can be changed:  

Property | Default | Description
--- | --- | ---
`docker.from.image` | openjdk | Docker image to build your application `from`
`docker.from.tag` | 8u181-jdk-slim-stretch | Tag for the Docker image `from`
`docker.container.port` | 8080 | Port that the container exposes at runtime

#### Build Docker Image
You can also use `mvn package` in order to build your image directly to a Docker daemon.
For more information please refer to the [plugin documentation](https://github.com/GoogleContainerTools/jib/blob/master/jib-maven-plugin/README.md#build-to-docker-daemon).

If you want to disable the plugin add the argument `-Djib.skip=true` when you use `mvn` on the command line.

If you experience timeouts, you can set the property `jib.httpTimeout` to a value larger than the default of 20s on the command line (e.g. `-Djib.httpTimeout=60000` for 60s). At the time of writing, this property is not available as a build configuration parameter, so it has to be added manually. For more information please refer to [System Properties](https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin#system-properties).

# Legal
This project is available under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0.html).

Copyright 2019-2025 Expedia, Inc.
