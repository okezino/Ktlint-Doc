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
disabledRules this is ues to disable dome of the ktlint rules

```
ktlint{
    android = true
    ignoreFailures = false
    disabledRules = [""]
    reporters{
        reporter "plain"
        reporter "checkstyle"
        reporter "sarif"

    }
}
```

## Auto Format Styling
To auto format your code run 
```
./gradlew ktlintFormat
```
To auto add ktlintFormat to the prebuild when ever you run your application add the below code to your Module gradle file 

```
tasks.getByName("preBuild").dependsOn("ktlintFormat")
```


