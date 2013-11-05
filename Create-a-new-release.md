Release candidate (branch "develop")
------------------------------------
1. Update file [version.txt](/MovingBlocks/TerasologyLauncher/blob/develop/version.txt)

    Example: 1.1.0-rc

2. Update file [CHANGELOG.md](/MovingBlocks/TerasologyLauncher/blob/develop/CHANGELOG.md)

    Example: 1.1.0 (2013-10-27, unreleased)

3. Build jenkins job [TerasologyLauncherNightly](http://jenkins.movingblocks.net/view/Launcher/job/TerasologyLauncherNightly/)

    View test and check results

    Download and test created version

Prepare release (branch "develop", local git workspace)
-------------------------------------------------------
1. Update file [version.txt](/MovingBlocks/TerasologyLauncher/blob/develop/version.txt)

    Example: 1.1.0

2. Update file [CHANGELOG.md](/MovingBlocks/TerasologyLauncher/blob/develop/CHANGELOG.md)

    Example: 1.1.0 (2013-10-27)

3. Commit both files

    Example: "Release 1.1.0"

4. Create a tag

    Example: git tag 'v1.1.0'