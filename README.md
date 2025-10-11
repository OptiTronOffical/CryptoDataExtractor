`Desktop`) and limits the search depth in less important ones.

- **Reliable architecture**:
    - **Object-oriented design**: The code is divided into logical classes (`CryptoDataExtractor`, `CryptoFileAnalyzer`, `TelegramSender`).
    - **Error handling and logging**: Detailed logging of all operations to the console and the `crypto_extractor.log` file, as well as reliable exception handling.

- **Integration with Telegram**:
    - **Structured Reports**: Sends results as separate, clearly labeled files.
    - **Secure Send**: Enables retry mechanisms for reliable message delivery.
    - **Large file handling**: If the archive with files exceeds Telegram's limit, the script will send a text list of the most important finds.

---

## 🏗️ Architecture

The project is built on the principles of object-oriented programming to ensure modularity and scalability.

- **`CryptoDataExtractor`**: The main class that organizes the entire process: from extracting data from browsers to calling the analyzer and sending the results.
- **`CryptoFileAnalyzer`**: The "brain" of the system. This class is responsible for complex and precise file analysis. It contains all the logic for identifying "cryptocurrency" files, the evaluation system, and exclusion rules.
- **`TelegramSender`**: Encapsulates all the logic for interacting with the Telegram Bot API, including sending messages, documents, and handling network errors.
- **Dataclasses** (`BrowserCredential`, `CryptoFile`): Used to store data in a strict and structured manner, making the code more readable and reliable.
