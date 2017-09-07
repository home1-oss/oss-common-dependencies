
# oss-common-dependencies-spring-boot-1.5.x
Define and constraint version of spring family and third party modules, based on spring-boot-1.5.x.

Sub projects may override dependencies defined here.  

spring family modules:
+ spring-boot
+ spring-data-releasetrain
+ spring-io-platform
+ spring-cloud

## Rules when maintaining pom files

- Versions defined in `properties` tag should in format like `<${artifactId}-version>${artifactVersion}</${artifactId}-version>`.
  Sort by dictionary order as possible for easier to locate.

- Third party dependencies in `dependencyManagement->dependencies` tag need to be sorted by dictionary order as possible for easier to locate.
