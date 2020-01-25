# Base POM for Java Projects
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) 
![](https://img.shields.io/badge/Package-POM-2396ad)
![](https://img.shields.io/badge/Repository-Maven%20Central-2396ad)  
![](https://github.com/wigforss/java-base-pom/workflows/Test%20and%20Deploy/badge.svg)

Maven base parent POM for Java projects.

```
<parent>
    <groupId>org.kasource</groupId>
    <artifactId>java-base-pom</artifactId>
    <version>0.3</version>
</parent>
```

Set common tags such as:
* licenses
* organization
* developers 
* issueManagement
* ciManagement
* distributionManagement

Provides plugin management for basic plugins and plugin configurations needed to perform release to [OSSRH](https://oss.sonatype.org/)

## JDK Version
The default JDK version is 11.

JDK version to use can be specified with the maven property **jdk.version**. Override in child POMs to change JDK version. 

```
 <properties>
     <jdk.version>11</jdk.version>
 </properties>
```
## SCM
SCM is configured by properties (given artifactId is the same as the repository name), add the following the child POMs.

```
<scm>
    <connection>${scm.connection.url}</connection>
    <developerConnection>${scm.connection.url}</developerConnection>
    <url>${scm.url}</url>
    <tag>HEAD</tag>
</scm>
```


