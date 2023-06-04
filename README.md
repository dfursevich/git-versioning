Playing with [Maven versioning extension](https://github.com/qoomon/maven-git-versioning-extension)

The artifact version is derived from git (branch or tag), the version in pom.xml
is ignored.

To get the current version run:
`mvn help:evaluate -Dexpression=project.version -Dorg.slf4j.simpleLogger.log.me.qoomon.maven.gitversioning=debug`

##### How it works

1. If you are on branch the version will be the most recent tag + 1 in patch version
e.g. tag v0.0.1 -> 0.0.2-SNAPSHOT
2. If you are on tag the version will be equal to this tag e.g. tag v0.0.1 -> 0.0.1

