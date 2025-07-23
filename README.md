# Kotlin Telegram Echo Bot Project

## Overview
This project is a simple Kotlin application designed to run a Telegram echo bot. The bot listens for incoming messages and replies with the same text, effectively "echoing" what users send to it.

## Project Structure
```
src/main/kotlin/
├── EchoBot.kt   # The bot implementation
└── Main.kt      # The application entry point
```

### EchoBot.kt
- Defines the `EchoBot` class, which extends `TelegramLongPollingBot` from the Telegram Bots Java library.
- Handles incoming updates (messages) and sends back the same text to the user.
- Uses the Telegram Bot API to send and receive messages.

### Main.kt
- Contains the `main` function, which is the entry point of the application.
- Reads the bot token from the `TELEGRAM_BOT_TOKEN` environment variable.
- Instantiates the `EchoBot` and registers it with the Telegram Bots API.
- Handles any exceptions that occur during bot registration.

## How to Build and Run
**Note:** The current `build.gradle.kts` does not include the required Telegram Bot dependencies. You must add them to build and run the bot.

1. **Add the Telegram Bot Java library to your `build.gradle.kts`:**
   ```kotlin
   dependencies {
       implementation("org.telegram:telegrambots:6.5.0")
       implementation("org.telegram:telegrambots-meta:6.5.0")
   }
   ```
2. **Build the project:**
   ```sh
   ./gradlew build
   ```
3. **Run the project:**
   ```sh
   ./gradlew run
   ```
   Make sure to set the `TELEGRAM_BOT_TOKEN` and (optionally) `BOT_USERNAME` environment variables before running.

## Environment Variables
- `TELEGRAM_BOT_TOKEN`: Your bot's token from BotFather.
- `BOT_USERNAME`: (Optional) The username of your bot.

## Note
If you only want a Hello World app, remove all Telegram-related code and dependencies, and use a simple `main` function that prints to the console. 