# Maven Archetype for eXist Apps

This repository contains the code for a Maven Archetype for eXist Apps.

This archetype can be used to generate a skeleton project for building an eXist-db App (EXPath Package) using Maven.

## Usage

* Requirements: Java 8, Apache Maven 3.3+, Git.

Switch to a directory on your computer where you keep the projects, and then run Maven for this archetype to create a new project directory. e.g.:

```bash
$ cd my-projects
$ mvn archetype:generate \
    -DarchetypeGroupId=org.exist-db \
    -DarchetypeArtifactId=exist-apps-archetype \
    -DarchetypeVersion=1.0
```

Maven will then prompt you for a `groupId`, `artifactId`, and `version` for your project. e.g.:

```bash
Define value for property 'groupId': : com.myorganisation.existdb.app
Define value for property 'artifactId': : my-app1
Define value for property 'version':  1.0-SNAPSHOT: : 
Define value for property 'package':  com.myorganisation.existdb.app: : 
Confirm properties configuration:
groupId: com.myorganisation.existdb.app
artifactId: my-app1
version: 1.0-SNAPSHOT
package: com.myorganisation.existdb.app
 Y: : y
```

You will then have a new directory named after the `artifactId` of your project, e.g.: `my-app1`.

NOTE: The project is setup to expect to be under Git version control. If you are not already in a Git repository, you should create one:

```bash
$ cd my-app1
$ git init
$ git add pom.xml src/ xar-assembly.xml xquery-license-style.xml LICENSE README.md
$ git commit -m "Start of my eXist-db App"
```
