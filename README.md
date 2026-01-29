# Chat-App

Chat-App is a **multithreaded chat-room** application developed in C++ using the *Boost.Asio* library. It demonstrates a robust, asynchronous server–client architecture that supports multiple chat sessions concurrently and handles real-time messaging efficiently across many clients.

The server manages multiple client connections and routes messages between them. Each client can send and receive messages in the chat room. The server broadcasts messages to all connected clients; the chat session receives messages from clients and forwards them to the server. The design uses the asynchronous I/O model provided by Boost.Asio for high performance and scalability.

## Project Structure

```
Chat-App/
├── chatClient/
│   ├── async_client.cpp    # Client implementation
│   └── echo_client.cpp     # Use for testing
├── chatServer/
│   ├── async_server.cpp    # Server implementation
│   └── echo_server.cpp     # Use for testing
├── networkLibrary/
│   ├── networkLibrary.h    # Network library header
│   └── networkLibrary.cpp  # Network library implementation
├── utils/
│   ├── Logger.h            # Logger utility header
│   └── Logger.cpp          # Logger utility implementation
└── CMakeLists.txt          # Root CMake configuration
```

## Components

- **chatClient** — Client module that communicates with the server.
- **chatServer** — Server module that handles multiple clients asynchronously.
- **networkLibrary** — Library that encapsulates network communication logic.
- **utils** — Utility module providing logging across the application.

## Requirements

- C++17 or later
- A C++ compiler with C++17 support (e.g., g++, clang++)
- CMake 3.10 or higher
- Git (for cloning the repository)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/suryansh101gupta/ChatApp.git
cd Chat-App
```

### 2. Build the Project

```bash
# Create a build directory
mkdir build
cd build

# Configure with CMake
cmake ..

# Build
cmake --build .
```

### 3. Run the Executables

**Server:**

```bash
./chatServer/asyncServer <SERVER_PORT>
```

**Client:**

```bash
./chatClient/asyncClient <SERVER_IP> <SERVER_PORT>
```

### 4. Clean Up

To remove build artifacts:

```bash
cd build
cmake --build . --target clean
```

## Contributing

Contributions are welcome. Please fork the repository and open a pull request with your changes. Ensure your code matches the existing style and that all tests pass before submitting.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
