# **Botel - Telegram Bot Library in Go**

**Botel** is a powerful and easy-to-use Telegram bot library built in Go, providing seamless integration with the Telegram Bot API. It enables developers to create feature-rich Telegram bots with minimal effort, including message handling, media management, and advanced interactions.

### Key Features:
- **Message Interaction**: Send and receive text messages, photos, files, and videos.
- **User Information Retrieval**: Access user details of those interacting with your bot.
- **Group & Channel Management**: Manage messages, members, and various tasks within groups and channels.
- **Media & Files**: Upload and download various file formats, including images, videos, and documents.
- **Command Handling**: Define custom commands that respond to specific user inputs.
- **Webhooks Support**: Receive real-time updates with webhooks for efficient interaction.
- **Classifier Support**: Automatically categorize and respond to messages using machine learning algorithms.
- **Rate Limits Management**: Handle API rate limits and display the allowed request counts and reset times.
- **Bot Status Management**: Display different statuses such as "active," "inactive," or "processing."
- **Custom Menus & Commands**: Create custom menus and complex user interactions.
- **Multilingual Support**: Build bots that can handle multiple languages for international users.
- **Caching for Performance**: Use caching to enhance response times and reduce server load.
- **Message Filtering & Categorization**: Apply AI algorithms to identify and filter messages for automatic replies.
- **Advanced Methods**: Supports advanced Telegram methods like Inline Queries and Callback Queries.
    - **Inline Queries**: Perform searches and interactions directly within chats without the need for direct messages to the bot.
    - **Callback Queries**: Interact with inline buttons and menus that the bot responds to.
- **GPS & Location Data**: Send and receive geographic location data of users.
- **Image & Video Processing**: Leverage tools to edit or convert images and videos before sending them.

---

## **Installation**

To get started with **Botel**, follow the installation steps below:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/hadirezaei1377/botel.git
    ```

2. **Install dependencies**:
    ```bash
    cd botel
    go mod tidy
    ```

3. **Set up your Telegram Bot API token**:
   - Create a bot on Telegram through [BotFather](https://core.telegram.org/bots#botfather) and get the token.
   - Set the token in your environment variables or pass it directly to the bot constructor.

---

## **Usage**

Here’s a simple example to get started with **Botel**:

```go
package main

import (
    "github.com/yourusername/botel"
    "log"
)

func main() {
    bot, err := botel.NewBot("YOUR_API_TOKEN")
    if err != nil {
        log.Fatal(err)
    }

    bot.Handle("/start", func(msg *botel.Message) {
        bot.SendMessage(msg.Chat.ID, "Welcome to Botel!")
    })

    // Run bot
    bot.Start()
}
```

## **Contributing**

We welcome contributions to **Botel**. If you’d like to contribute, please fork the repository and create a pull request with your changes.

1. Fork the repository
2. Clone your fork
3. Create a new branch for your feature
4. Commit your changes
5. Push to your fork
6. Open a pull request

---

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


