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
    -DarchetypeVersion=1.9
```

Maven will then prompt you for a `groupId`, `artifactId`, `version`, and `package` for your project. You need only specify the `groupId` and `artifactId`, for the others you may accept the defaults.

* `groupId` is similar to a Java package name. If you are going to publish your XAR publicly it should be some sub-coordinate of a domain name that you have responsibility for supplied in reverse order notation. For example, if your company is "*My Organisation Ltd*" you might own the domain name `myorganisation.com`, you might decide that a suitable sub-domain for your eXist-db Apps might be `app.existdb.myorganisation.com`. **Note:** this sub-domain does not have to be able to be de-referenced.

* `artifactId` is just a simple name without spaces for the App itself. Together the `groupId:appId` must be unique.

* `version` almost speaks for itself. In Maven `-SNAPSHOT` are development versions. Your first version should always be `1.0-SNAPSHOT`, with the first release subsequently being `1.0`.  


e.g.:

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

You should now consult the `README.md` of your `my-app1` for further instructions and documentation.
