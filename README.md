[![Build Status](https://travis-ci.org/lamba92/dbn-particle-tester.svg?branch=master)](https://travis-ci.org/lamba92/dbn-particle-tester) [![](https://jitpack.io/v/lamba92/dbn-particle-tester.svg)](https://jitpack.io/#lamba92/dbn-particle-tester)

# DBN PARTICLE TESTER

This library shows an inference example on a [aima](https://github.com/aimacode/aima-java)'s `DynamicBayesianNetwork` using particle filtering. 

## Installing

Add the [JitPack.io](http://jitpack.io) repository to the project `build.grade`:
```
repositories {
    maven { url 'https://jitpack.io' }
}
```

Then import the latest version in the `build.gradle` of the modules you need:

```
dependencies {
    implementation 'com.github.lamba92:dbn-particle-tester:{latest_version}'
    implementation 'com.googlecode.aima-java:aima-core:3.0.0'
}
```

If using Gradle Kotlin DSL:
```
repositories {
    maven(url = "https://jitpack.io")
}
...
dependencies {
    implementation("com.github.lamba92", "dbn-particle-tester", "{latest_version}")
    implementation("com.googlecode.aima-java", "aima-core", "3.0.0")
}
```

If you are using Maven:
```
<repositories>
	<repository>
	    <id>jitpack.io</id>
	    <url>https://jitpack.io</url>
	</repository>
</repositories>
```
```
<dependency>
    <groupId>com.github.lamba92</groupId>
    <artifactId>dbn-particle-tester</artifactId>
    <version>0.1</version>
</dependency>
```

## Usage

To compute che distribution of the two networks at a given moment you have to call `it.unito.UmbrellaParticle.main(particles, vararg evidences)` where `particles` is the number of samples (recommended a number between 1000 and 10000), `evidences` is a variable number of `0`s and `1`s where `0` means to set false the evidences and `1` set them to true on that specific iteration.

## Authors

* **Gianluca Torta** - [giatorta](https://github.com/giatorta)
