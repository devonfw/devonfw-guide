
# devonfw guide

This repository contains a collection of guides and documents from the different devonfw's modules, such as:

* **cicdgen**: Tool for generating CI/CD configurations for devonfw projects.
* **devon4j**: Module for Java
* **devon4net**: Module for .net
* **devon4ng**: Module for Angular
* **devonfw shop floor**: Set of documentation, tools and methodologies used to configure provisioning, development and uat environments used in devonfw projects.
* **devonfw testing**: Module for testing.
* **My Thai Star**: devonfw reference application.


## How is this guide organized

Each submodule contains a master file *name-of-the-wiki.wiki/master-name-of-the-wiki.asciidoc* which includes all the other files in the submodule. All master-*.asciidoc files are joined in *devonfw-guide/master.asciidoc*, this way, all documents are linked and can be used to generate a unique file.

## How to generate a PDF

### Necessary set up

* master files
* maven
* docgen 
    * Added as maven dependency so it gets downloaded from maven repository
    * Downloading it from [its git repository](https://github.com/devonfw/devon-docgen)
    * A forked version with corrections can be found at https://github.com/jambulud/devon-docgen/tree/pom-upgrades

* pom.xml pointing to master

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.devonfw</groupId>
  <artifactId>devonfw-guide-tutorial-sources-wiki</artifactId>
  <version>dev-SNAPSHOT</version>
  <packaging>pom</packaging>
  <name>devonfw guide</name>

  <parent>
    <groupId>com.devonfw.tools</groupId>
    <artifactId>devon-docgen</artifactId>
    <version>3.1.1-SNAPSHOT</version>
  </parent>

  <properties>
    <docgen.wiki.page>master</docgen.wiki.page>
  </properties>

</project>
```

---
**TIP**

**version** tag under **parent** should specify the current docgen version. Newer versions could include bug fixes.

---


If you want to use your own docgen version you have to add its pom.xml file in devonfw-guide's parent directory:

* pom.xml (docgen)
* devonfw-guide
    * pom.xml (guide, pointing to master)
    * name-of-the-wiki-1
        * master-name-of-the-wiki-1
    * name-of-the-wiki-2
        * master-name-of-the-wiki-2
    * name-of-the-wiki-n
        * master-name-of-the-wiki-n



### Generate the PDF

To generate a PDF of this guide using docgen you have to:

* Download or clone this repository.
* Run the command below in a console:

```bash
route-to-devonfw-guide$ mvn clean package
```

The result can be found at *devonfw-guide/target/generated/docs*


---
**IMPORTANT**

If your directory contains huge amounts of files, maven can throw a OutOfMemoryError. More info at [Maven OutOfMemoryError](https://cwiki.apache.org/confluence/display/MAVEN/OutOfMemoryError)

---

