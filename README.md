# Common Checkstyle Config

<img src="https://github.com/patrickfav/checkstyle-config/blob/master/misc/icon_sm.png?raw=true" align="right"
     alt="Logo" width="128" height="128">

Externalized checkstyle configuration which can be used in other Maven projects.

[![Download](https://api.bintray.com/packages/patrickfav/maven/checkstyle-config/images/download.svg)](https://bintray.com/patrickfav/maven/checkstyle-config/_latestVersion)
[![Build Status](https://travis-ci.com/patrickfav/checkstyle-config.svg?branch=master)](https://travis-ci.com/patrickfav/checkstyle-config)

## Description

This is a hand-picked, incrementally improved checkstyle configuration. It is more on the liberal side as I believe tools should work for the user not the other way around. Code style is subjective and this one might not be for you.

## Usage

Add this maven project as dependency to load the external checkstyle configuration. The name of the config xml is `checkstyle.xml`.

```xml
    <build>
        <plugins>
            <!-- checkstyle -->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-checkstyle-plugin</artifactId>
                ...
                <dependencies>
                    ...
                    <!-- add this lib as dependency to load external checkstyle config -->
                    <dependency>
                        <groupId>at.favre.lib</groupId>
                        <artifactId>checkstyle-config</artifactId>
                        <version>{latest_version}</version>
                    </dependency>
                </dependencies>
                <configuration>
                    <configLocation>checkstyle.xml</configLocation>
                </configuration>
            </plugin>
            ...
```

See this [stackoverflow.com post](https://stackoverflow.com/a/19690484/774398) for more info.

### IDE Integration

#### IntelliJ

If you are using the [checkstyle plugin](https://plugins.jetbrains.com/plugin/1065-checkstyle-idea) for [IntelliJ](https://www.jetbrains.com/idea/) (which you should). You will find a copy of the configuration in the `/target` folder called `checkstyle-checker.xml`. 

# License

Copyright 2019 Patrick Favre-Bulle

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
