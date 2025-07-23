# How to Build and Run This Project

## Building the Project
To compile the Kotlin project, open a terminal in the project root and run:

```sh
./gradlew build
```
- This command uses the Gradle wrapper to download dependencies (if any), compile the code, and produce build outputs in the `build/` directory.
- You do **not** need to have Gradle installed globally; the wrapper (`./gradlew`) handles everything.

## Running the Project
To run the application (which prints `Hello, world!`), use:

```sh
./gradlew run
```
- This will execute the `main` function in `Main.kt`.
- The output should be:
  ```
  Hello, world!
  ```

## Purpose of `Main.kt`
- `Main.kt` is the entry point of your Kotlin application.
- It contains the `main` function, which is the first code that runs when you start the app.
- In this project, `Main.kt` simply prints `Hello, world!` to the console, serving as a minimal example of a working Kotlin program.

---

**Summary:**
- Use `./gradlew build` to compile the project.
- Use `./gradlew run` to execute the app.
- `Main.kt` is where your program starts and currently just prints a greeting. 