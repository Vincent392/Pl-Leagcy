# Rosepad Server&Client

Rosepad is a custom Lilypad QA server/client based on [Smaed's unofficial jars](https://github.com/AlphaVerUnofficialJars)
focused on adding new features to the game.
Preview Loader is a fork as a attempt port of Rosepad To
Alpha 1.0.16.05 Preview and Alpha 1.0.16.05 UNR.PREVIEW2 

## Installation

- Install both JDK 8 and JDK 17
- Clone this repository
- Run `TOOLKIT_JAVA17=/path/to/your/jdk17/home ./gradlew -Dorg.gradle.java.home=/path/to/your/java8/home prepare injectClasses processPatches shadowJar pack` and wait for build to finish

> /!\ Caution /!\
> You may have to re-run build several times for it to succeed.
> If you encounter `java.lang.IllegalStateException: An error occurred while decompiling this method.` in runtime, try rebuilding Rosepad.

## Running

To test Rosepad, you must set it up and run `./gradlew -Dorg.gradle.java.home=/path/to/your/java8/home build runClient`.

For the server, run `./gradlew -Dorg.gradle.java.home=/path/to/your/java8/home build runServer`.

## Contributing

Since Minecraft is not licensed under a free software license, we can't share its source code, any modifications
must be stored in .patch files (at least until proper code injections will be implemented) Make sure to test your
patches before making a pull request

Build Rosepad use `TOOLKIT_JAVA17=/path/to/your/jdk17/home ./gradlew -Dorg.gradle.java.home=/path/to/your/java8/home ejectClasses createPatches shadowJar pack`

All tests should be done on an obfuscated build since obfuscation breaks some things in the code

