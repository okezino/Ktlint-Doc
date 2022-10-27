# Ktlint-Doc

Ktlint is use to enforce coding guidelines and maintain standard, Kitlint is an Android Gradle plugin that runs to analysis for well structured code .

It tells you the line that have formatting issues

## Dependency 
Add this to your Gradle plugin 
```
id 'org.jlleitschuh.gradle.ktlint' version "11.0.0"
```
## Styling
android set to true donates setting the ktlint 
ignoreFailures false donate on running the .gradlew ktlintCheck 

```
ktlint{
    android = true
    ignoreFailures = false
    reporters{
        reporter "plain"
        reporter "checkstyle"
        reporter "sarif"

    }
}
```
