# Maven Central parent POM
Parent POM file with plugins necessary for Maven Central deployments.

## Using this parent POM
In order to use this pom set it as parent in target Maven POM file and use ``maven-central`` profile when building.

## Maven properties
Maven properties which can be set to change build behaviour.

### Required properties
* **maven-gpg-plugin.key-name** - a name of gpg key used to sign artifacts.
    This key needs to be present in GPG home directory.

### Optional parameters
Defining behaviour:
* **maven-sonatype-plugin.auto-release** - [true/false] defines whether deployed artifacts
   should automatically be released. **Default**: true,
* **maven-checksum-plugin.version** - an identifier of the Sonatype server configured in settings.xml
  to publish artifacts to. **Default**: ossrh,
* **maven-sonatype-plugin.nexus-server** - url of Sonatype Nexus server.

Defining plugin dependency versions:
* **maven-checksum-plugin.version** - a version of Maven checksum plugin. **Default**: check POM for details,
* **maven-gpg-plugin.version** - a version of Maven gpg plugin. **Default**: check POM for details,
* **maven-javadoc-plugin.version** - a version of Maven javadoc plugin. **Default**: check POM for details,
* **maven-sonatype-plugin.version** - a version of Maven sonatype plugin. **Default**: check POM for details,
* **maven-source-plugin.version** - a version of Maven source plugin. **Default**: check POM for details.