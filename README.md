# Chat-App (Multithreaded Chat Room in C++)

**Chat-App** is a high-performance, **multithreaded chat-room application** developed in **C++** using the **Boost.Asio** library. The project demonstrates a robust **asynchronous client–server architecture** capable of handling multiple concurrent chat sessions efficiently.

The application leverages Boost.Asio’s **non-blocking I/O model** to ensure scalability, responsiveness, and efficient real-time communication between multiple connected clients.


---

## ✨ Features

- Asynchronous, non-blocking networking using **Boost.Asio**
- Multithreaded server supporting **multiple concurrent clients**
- Real-time message broadcasting to all connected clients
- Modular and reusable networking library
- Dedicated echo client/server for testing
- Thread-safe logging utility
- Cross-platform build support using **CMake**

---

## 🏗 Architecture Overview

The application follows a **client–server architecture**:

- The **Server** accepts multiple client connections and manages each session asynchronously.
- **Clients** send messages to the server without blocking execution.
- The server **broadcasts messages** to all active clients.
- Networking logic is abstracted into a reusable **networkLibrary** module.
- Logging is centralized via a utility logger for debugging and monitoring.

This architecture ensures scalability and efficient resource utilization under concurrent loads.

---

## 📁 Project Structure

```text
chatClient/
 ├── async_client.cpp         # Asynchronous client implementation
 ├── echo_client.cpp          # Client used for testing

chatServer/
 ├── async_server.cpp         # Asynchronous server implementation
 ├── echo_server.cpp          # Server used for testing

networkLibrary/
 ├── networkLibrary.h         # Networking library header
 ├── networkLibrary.cpp       # Networking library implementation

utils/
 ├── Logger.h                 # Logger utility header
 ├── Logger.cpp               # Logger utility implementation

CMakeLists.txt                # Root CMake configuration
