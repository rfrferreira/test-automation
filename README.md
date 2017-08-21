# Test Automation

In order to start building my small Java automation projects I need to start right here.

## First things first

If you're using MacOS, you should start by installing [Homebrew](https://brew.sh/). Homebrew aka *"The missing package manager for MacOS"* let's you install all the stuff that Apple didn't.

After this, and to make my project dependencies easier to manage I install [Gradle](https://gradle.org/install/).

Then, when you create you Java project with Gradle, you're able to manage your dependencies easy mode in your build.gradle file.

Just like this, I can have all the dependencies I need to my project available:

```Java

group 'testautomation'
version '1.0-SNAPSHOT'

apply plugin: 'java'

sourceCompatibility = 1.8

repositories {
    mavenCentral()
}

dependencies {
    testCompile group: 'junit', name: 'junit', version: '4.12'

    // https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java
    compile group: 'org.seleniumhq.selenium', name: 'selenium-java', version: '2.41.0'

    // https://mvnrepository.com/artifact/org.assertj/assertj-core
    testCompile group: 'org.assertj', name: 'assertj-core', version: '3.8.0'

    // https://mvnrepository.com/artifact/org.testng/testng
    testCompile group: 'org.testng', name: 'testng', version: '6.11'

    // https://mvnrepository.com/artifact/info.cukes/cucumber-java
    compile group: 'info.cukes', name: 'cucumber-java', version: '1.2.5'

    // https://mvnrepository.com/artifact/info.cukes/cucumber-core
    compile group: 'info.cukes', name: 'cucumber-core', version: '1.2.5'

    // https://mvnrepository.com/artifact/info.cukes/cucumber-junit
    testCompile group: 'info.cukes', name: 'cucumber-junit', version: '1.2.5'

    // https://mvnrepository.com/artifact/info.cukes/gherkin
    provided group: 'info.cukes', name: 'gherkin', version: '2.12.2'

    // https://mvnrepository.com/artifact/io.cucumber/gherkin
    compile group: 'io.cucumber', name: 'gherkin', version: '4.1.3'
}
```
