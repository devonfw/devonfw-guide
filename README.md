# devonfw guide

---

**IMPORTANT**

Download the **continuously updated devonfw guide** from [here](https://github.com/devonfw/devonfw-guide/raw/master/devonfw_guide.pdf).

---

This repository contains a collection of guides and documents from different _devonfw_ modules:

- **getting started**: Standalone introduction guide.
- **ide**: devonfw IDE.
- **devon4j**: Module for Java
- **devon4ng**: Module for Angular
- **devon4net**: Module for .NET
- **devon4node**: Module from Node.js
- **database**: Information on selecting a suitable database.
- **devonfw shop floor**: Set of documentation, tools and methodologies used to configure provisioning, development and uat environments used in devonfw projects.
- **cicdgen**: Tool to generate CI/CD configurations for devonfw projects.
- **production line**: Templates and info on setting up a Jenkins PL.
- **CobiGen**: Code-based incremental generator.
- **MrChecker**: E2E testing framework.
- **MyThaiStar**: devonfw reference application.
- **contributing**: Contributing and OSS compliance guidelines, community code of conduct. 
- **release notes**: Chagelogs and feature-lists of devonfw releases.

## How this guide is organized

Each submodule contains a master file `name-of-the-wiki.wiki/master-name-of-the-wiki.asciidoc` which includes all the other files in the submodule. All `master-*.asciidoc` files are joined in `devonfw-guide/master.asciidoc`. This way, all documents are linked and can be used to generate a complete file.

## How to generate a PDF

Please find the documentation how to generate a PDF for your project/wiki in the [docgen repository](https://github.com/devonfw/docgen/wiki#usage).

**IMPORTANT**

If your directory contains a large amount of files, Maven might throw an `OutOfMemoryError`. For information on how to fix this issue please refer to: [Maven OutOfMemoryError](https://cwiki.apache.org/confluence/display/MAVEN/OutOfMemoryError).
