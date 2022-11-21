Updated repo for [How to improve the quality of tests using mutation testing](https://medium.com/@inzuael/how-to-improve-the-quality-of-tests-using-mutation-testing-2346019829f1) article.

## Run Mutation Tests

Cmd 
`./gradlew pitest --rerun-tasks` (`--rerun-tasks` flag is required to display cmd output in the following runs)

or

[PIT Mutation Testing](https://plugins.jetbrains.com/plugin/7119-pit-mutation-testing) IDEA plugin 
`Run->Edit Configurations->Defaults->Pit Runner`

## Setup

1. [PIT](https://pitest.org/)
```
pitest {
    setProperty("pitestVersion", "1.9.0")
    ...
}
```

2. [pitest-junit5-plugin](https://github.com/pitest/pitest-junit5-plugin) - adds support to pitest for JUnit 5 and the Jupiter api
   (requires specific versions of `JUnit` add `pitest` ):

```
pitest {
    setProperty("junit5PluginVersion", "1.1.0")
    ...
}
```

1. [gradle-pitest-plugin](https://github.com/szpak/gradle-pitest-plugin) - provides an ability to perform a mutation testing and calculate a mutation coverage of a Gradle-based projects with PIT

```
id("info.solidsoft.pitest") version "1.9.0"
```
