checkstyle-xml-config
=====================

Checkstyle is a development tool to help programmers write Java code that adheres to a coding standard. It automates the process of checking Java code to spare humans of this boring (but important) task. This makes it ideal for projects that want to enforce a coding standard.

This repo contains the NFL checkstyle xml config files used by Gradle, IntelliJIDEA and Eclipse.

# Gradle install

```
apply plugin: 'checkstyle'
check.dependsOn 'checkstyle'

task checkstyle(type: Checkstyle) {
    configFile file("${project.rootDir}/config/checkstyle/sun_checks.xml")
    source 'src'
    include '**/*.java'
    exclude '**/gen/**'

    classpath = files()
}
```
