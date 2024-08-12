# Spring Boot Parent

This is the parent for all Maven based Spring Boot projects in Axians Netherlands. It contains the common settings and plugins for all projects.

## Usage
To use this parent, add the following to your project's `pom.xml`:
```xml
<parent>
    <groupId>nl.axians</groupId>
    <artifactId>spring-boot-parent</artifactId>
    <version>5</version>
</parent>
```

You can update the Spring Boot version by overriding the `spring-boot.version` property. This parent has the [axians](https://github.com/axians-oss/axians-parent) über parent as its parent with all its settings and plugins.


## License
This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE.md) file for details.


