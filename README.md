# Multi-Threaded TCP Server in Rust

This project implements a multi-threaded TCP server in Rust, capable of handling concurrent connections using a thread pool.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Starting the Server](#starting-the-server)
  - [Configuration](#configuration)
- [How It Works](#how-it-works)

## Features

- **Thread Pool**: Utilizes a thread pool to manage concurrent connections efficiently.
- **Graceful Shutdown**: Supports graceful shutdown, ensuring all connections are handled properly.
- **Customizable Configuration**: Allows easy configuration of server settings such as the listening address and port.

## Getting Started

### Prerequisites

Make sure you have Rust and Cargo installed on your system. You can install Rust and Cargo by following the instructions [here](https://www.rust-lang.org/tools/install).

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/0xsaksham/multi_thread_server.git
   ```

2. Navigate to the project directory:

   ```bash
   cd multi_thread_server
   ```

3. Build the project:

   ```bash
   cargo build --release
   ```

## Usage

### Starting the Server

To start the server, run the following command:

```bash
cargo run
```

By default, the server listens on `127.0.0.1:7878` or `localhost:7878`.

### Configuration

You can modify the server settings, such as the listening address and port, in the `main.rs` file. Additionally, you can adjust the size of the thread pool according to your requirements.

## How It Works

The server utilizes a thread pool to handle incoming connections concurrently. When a client connects, a worker thread from the pool is assigned to handle the connection. This allows the server to process multiple requests simultaneously without blocking.