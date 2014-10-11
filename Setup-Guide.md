<img align="left" width="96px" src="images/setup.png"/>
__TerasologyLauncher__ uses a [Gradle](http://gradle.org)-based build system and provides a [wrapper](gradle.org/docs/current/userguide/gradle_wrapper.html) `gradlew`. The wrapper is a script which is called from the root of the source tree. It downloads and installs [Gradle](http://gradle.org) automatically.
Depending on the system it may be necessary to `./graldew` instead of plain `gradlew`.

## Overview
Basically everything can be done using the [Gradle](http://gradle.org) wrapper. The following list is an excerpt of some tasks you are most likely to use.

| Command               | *Description* |
|:----------------------|:--------------|
|`gradlew build`        | *Compile the source doe, run tests, and build a JAR.* |
|`gradlew install`      | *Create a runnable installation locally (placed in `./build/install/TerasologyLauncher`).* |
|`gradlew run`          | *Build and run the launcher.* |
|`gradlew createRelease`| *Create a local development release (located in `./build/distributions`).* |
|`gradlew tasks`        | *Display available build script tasks.* |

## Initial Setup
To be able to run **TerasologyLauncher** from source follow these steps. This guide is designed for [IntelliJ IDEA](http://www.jetbrains.com/idea/) (you can use the free community edition), but alternative setups are possible.
If you have not done it yet, please download and install a recent [Java SDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html) - [Java SE 7u67](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) is currently recommended, although we are going to update to Java 8 soon.
Furthermore, you will need [Git](https://git-scm.com) for source control and sign up for [GitHub](https://github.com/signup/free).

### Step 1 - Fork the project
To get ready to tinker with the source code. First, *fork* the project by opening the [**TerasologyLauncher**](https://github.com/MovingBlocks/TerasologyLauncher) GitHub page and click on the little fork button in the upper right. 

### Step 2 - Clone the repo to your hard drive 
There are several ways to get the source code on your hard drive. You can either
- use the command line by executing `git clone https://github.com/MovingBlocks/TerasologyLauncher.git` (replace `MovingBlocks` with your GitHub username to use your own fork),
- use IntelliJ's feature "Check out from version control" and follow the prompts, or
- use [GitHub for Windows](https://windows.github.com/) or [GitHub for Mac](https://mac.github.com/) to clone the repo.

If you cloned your own fork you might want to set our repository as a remote. To do so, run

~~~
git remote add movingblocks https://github.com/MovingBlocks/TerasologyLauncher.git
~~~

### Step 3 - Generate project files and open in IntelliJ
To generate the project files for IntelliJ open a command prompt in the directory you checked out into and execute `gradlew idea` - this fetches the right version of Gradle and all project dependencies automatically plus it generates the project config. Afterwards, you can simply open the project file in IntelliJ. 

There is also a version for Eclipse - `gradlew eclipse` - but we encourage you to use IntelliJ.

## Development and Contribution
To get the latest changes from your remote repositories (e.g. `movingblocks`) you need to *fetch* all remote data via `git fetch --all`. This does not change your workspace, it just loads up your local Git database.

Make yourself familiar with Git's concept of repositories, branches, and commits. You can find some resources on how to use Git at the bottom of this page. 
 
Assume you have pushed some changes to your fork into a branch `myFeature`. In order to let us know about your work and give us the possibility to incorporate your changes you should send us a *pull request*. You can do this by selecting the `myFeature` branch on you GitHub repo and click the button which says "Open pull request". 

If you have further questions see the [[Community]] page and get in contact with us.

## Related Resources
Tutorials and further information on Git:
- htp://www.vogella.de/articles/Git/article.html
- http://gitref.org/
- http://progit.org/

Wiki pages of our main project [**Terasology**](https://github.com/MovingBlocks/Terasology) on developer setups:
- [Dev Setup](https://github.com/MovingBlocks/Terasology/wiki/Dev-Setup)
- [Fancy Git](https://github.com/MovingBlocks/Terasology/wiki/Fancy-Git)