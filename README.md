Useful Gradle Scripts
=====================

Various useful snippets of Gradle code that can be applied using:

```groovy
apply from:'http://gradle.smokejumperit.com/script-name.gradle'
```

You can also apply them directly from GitHub using the Raw view of the file. e.g.:

```groovy
apply from:'https://raw.github.com/RobertFischer/gradle-scripts/master/all-jars.gradle'
```

Or check out this directory onto your local box (e.g. `~/.gradle/RobertFischer/gradle-scripts`) 
and apply them that way.

```groovy
apply from:'~/.gradle/RobertFischer/gradle-scripts/all-jars.gradle'
```

The scripts to apply are below.

Add JavaDoc, Sources, and Test Jars to the Release
---------------------------------------------------

This uploads the JavaDoc, Sources, and Test jars as well as the straight source jar.

```groovy
apply from:'http://gradle.smokejumperit.com/all-jars.gradle'
```

Gaea (Gaelyk/Google App Engine API)
-------------------------------------

Bundles together all the configuration and tasks necessary to use [Gaelyk](http://gaelyk.appspot.com).

```groovy
apply from:'http://gradle.smokejumperit.com/gaea.gradle'
```

Smokejumper IT's Repository
------------------------------

Makes the Smokejumper IT repository available to your Gradle project.

```groovy
apply from:'http://gradle.smokejumperit.com/sjit_repo.gradle'
```

What Happend to GitHub-Dev and GitHub-Lib?
---------------------------------------------

GitHub got rid of downloads, so those scripts don't work anymore.
