# erchat

**erchat** is a simple yet powerful chat application written in **Erlang**. It showcases real-time messaging using Erlang’s concurrency strengths and lightweight processes, making it ideal for learning distributed programming and building reliable systems.

## Overview
**erchat** implements a basic multi-user chat system where clients can send messages to a server, which then broadcasts to connected clients. Built in pure Erlang, this project demonstrates core concepts like:
- Erlang processes and message passing
- OTP principles (lightweight concurrency)
- Server-client architecture
- Pattern matching and functional design

## Features
- Simple chat server handling multiple clients
- Broadcast messaging to all connected clients
- Text-based client interface
- Minimal dependencies
- Written entirely in Erlang

## Project Structure
```
├── db.erl # Simple in-memory storage module
├── erchat_client.erl # Chat client implementation
├── erchat_server.erl # Chat server logic
├── records.hrl # Data record definitions
├── ui.erl # User interface helpers
├── README.md # Project documentation
```

## Prerequisites
To build and run erchat, ensure you have:
- **Erlang/OTP** installed — version 24 or higher recommended  
  (Download from https://www.erlang.org/downloads)

## Getting Started
### 1. Clone the repository
```bash
git clone https://github.com/bitswright/erchat.git
cd erchat
```
### 2. Compile the code
- Start an Erlang shell:
  ```bash
  erl
  ```
- Compile all modules:
  ```erlang
  c(db).
  c(records).
  c(erchat_server).
  c(erchat_client).
  c(ui).
  ```
### 3. Run the Server
  ```erlang
  erchat_server:start().
  ```
### 4. Run a Client
- Open a new Erlang shell and start a client:
  ```erlang
  erchat_client:start().
  ```

## Usage
- Clients can type messages and press Enter to send. The server broadcasts messages to every connected client.
- Example:
  ```erlang
  [alice@erlang-shell] Hello everyone!
  ```

## Customization
- Feel free to extend:
  - Private messaging
  - Authentication or nicknames
  - Persistent message history
  - GUI frontend or web socket support

## License
This project is open source and available under the MIT License.
