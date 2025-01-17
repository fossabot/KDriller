# KDriller

[![GitHub license](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg?style=flat)](https://www.apache.org/licenses/LICENSE-2.0)
[![Maven Central](https://img.shields.io/maven-central/v/io.github.kevinah95/kdriller)](https://central.sonatype.com/artifact/io.github.kevinah95/kdriller)
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/io.github.kevinah95/kdriller?server=https%3A%2F%2Fs01.oss.sonatype.org)](https://s01.oss.sonatype.org/content/repositories/snapshots/io/github/kevinah95/kdriller)
[![Kotlin](https://img.shields.io/badge/kotlin-1.9.0-blue.svg?logo=kotlin)](http://kotlinlang.org)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fkevinah95%2FKDriller.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fkevinah95%2FKDriller?ref=badge_shield)

KDriller is a Kotlin framework that helps developers in analyzing Git repositories. With KDriller you can easily extract information about **commits**, **developers**, **modified files**, **diffs**, and **source code**. 

## About this repository

This project is a kotlin implementation of *PyDriller* by Davide Spadini, originally from
[PyDriller](https://github.com/ishepard/pydriller).

## Quick usage

```kotlin

import kdriller

val pathToRepo = listOf("https://github.com/ishepard/pydriller.git")
for(commit in Repository(pathToRepo).traverseCommits()){
        println(commit.hash)
        println(commit.msg)
        println(commit.author.name)
    }
```

## How to contribute
First clone the repository:
```
git clone https://github.com/kevinah95/kdriller.git
cd kdriller
```

**(Important)** I tend to not accept Pull Requests without tests, so:

- unzip the `test-repos.zip` zip file in `src/commonTest/resources/test-repos.zip`.
- inside are many "small repositories" that were manually created to test KDriller. Use one of your choice to test your feature (check the existing tests for inspiration)
- if none is suitable for testing your feature, create a new one. **Be careful**: if you create a new one, do not forget to upload a new zip file `test-repos.zip` that includes your new repository, otherwise the tests will fail.

To run the tests use gradle.

## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fkevinah95%2FKDriller.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fkevinah95%2FKDriller?ref=badge_large)