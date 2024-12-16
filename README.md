# Spring Boot Parent

This is the parent for all Maven based Spring Boot projects in Axians Netherlands. It contains the common settings and plugins for all projects. The current version of Spring Boot is `3.4.0`.

## Usage
To use this parent, add the following to your project's `pom.xml`:
```xml
<parent>
    <groupId>nl.axians</groupId>
    <artifactId>spring-boot-parent</artifactId>
    <version>9</version>
</parent>
```

You can update the Spring Boot version by overriding the `spring-boot.version` property. This POM has the [axians-parent](https://github.com/axians-oss/axians-parent) POM as its parent with all its settings, plugins and profiles.

### Building Spring Boot Native container image
To build a container image with a native spring Boot application you need to set the `skip.native.image` property to false. This will enable the `spring-boot-maven-plugin` to build a native image. Note that that docker must be running and the `spring-boot-maven-plugin` must defined in the `pom.xml` file of the application. The best way to do this is to specify the property on the command line:

```shell
mvn clean package -Dskip.native.image=false
```
### Setting the container registry
You can specify the container registry for the Spring Boot Native container image by setting the `container.registry` property. You can include sub-folders as well, e.g. `my-containers.registry.nl/project/`. The default value is `local`.

### Updating the native metadata repository
The native metadata repository is used to download metadata of popular frameworks that can be used during native image builds. You can update the version of the metadata repository by setting the `metadata-repository.version` property. The default value is `0.3.15`.

## License
This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE.md) file for details.


