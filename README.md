Gradle GitHub Development
===========================

This plugin enables support for development built on the GitHub infrastructure.

Using GitHub as a Maven Repository
-----------------------------------

You can use GitHub's Downloads section as a Gradle repository. This requires people
using your project to include GitHub in your project, and for you to get your files
into the upload section of GitHub. These both used to be a bit annoying, but this
plugin solves that problem.

First, for your clients. You can simply tell them to include this:

```groovy
apply from:'http://smokejumperit.com/github-libs.gradle'
```

Now, for you as the developer. First, in your build script, include this:

```groovy
group = 'MyGitHubUserName' // Replace with your GitHub username
version = '0.0.1' // Or whatever your version is

// After 'group' is set...
apply from:'http://smokejumperit.com/github-dev.gradle'

ghUpload {
	username = ... // If the code guesses the username wrong: see source for defaults
	password = ... // Or set Java prop 'github.password' or system env 'GITHUB_PASS'
}
```

Then you can run `gradle ghUpload` to upload your project and its pom to GitHub. 
This will also be done automatically as a part of `gradle uploadArchives`.

TODO
----

* It'd be nice to actually plug into the `uploadArchives` and the standard deployment
mechanisms. 
