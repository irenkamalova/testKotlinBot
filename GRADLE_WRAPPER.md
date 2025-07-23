# Gradle Wrapper: Purpose and Best Practices

## What is the Gradle Wrapper?
The Gradle Wrapper is a set of scripts and supporting files that allow anyone to build your project with a specific version of Gradle, **without requiring Gradle to be installed globally** on their machine.

## What files are included?
- `gradlew` (Unix shell script)
- `gradlew.bat` (Windows batch script)
- `gradle/wrapper/gradle-wrapper.jar` (the actual wrapper executable)
- `gradle/wrapper/gradle-wrapper.properties` (specifies the Gradle version and distribution URL)

## Why should you use and commit the wrapper?
- **Consistency:** Ensures everyone uses the same Gradle version, avoiding "works on my machine" problems.
- **Convenience:** New contributors can build the project immediately by running `./gradlew build` (or `gradlew.bat build` on Windows), without installing Gradle.
- **Automation:** CI/CD systems can build your project reliably, regardless of their pre-installed Gradle version.

## What should you commit?
- `gradlew`
- `gradlew.bat`
- The entire `gradle/wrapper/` directory (including `.jar` and `.properties`)

## What should you NOT commit?
- The `.gradle/` directory (local caches)
- The `build/` directory (build outputs)

## Summary
The Gradle wrapper scripts and the `gradle/wrapper/` directory are essential for making your project portable and easy to build for everyone. **Always commit them to version control.** 