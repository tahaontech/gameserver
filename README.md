# GameServer using Actor Model and WebSockets

This is a simple game server written in Go that leverages the actor model for efficient concurrency management and uses WebSockets for real-time communication with clients.

## Features

- Utilizes the actor model for concurrent and scalable game logic.
- Establishes WebSocket connections with clients for real-time communication.
- Easily extensible for implementing various multiplayer game mechanics.
- Demonstrates a basic framework for handling game state and player interactions.

## Requirements

- Go (version 1.10.1 or above)
- Any modern web browser supporting WebSockets.

## Installation and Usage

1. Clone this repository:

   ```
   git clone https://github.com/tahaontech/gameserver.git
   cd game-server
   ```

2. Build and run the server:

   ```
   make server
   ```

3. Access the game client by:

   ```
   make client
   ```

## Project Structure

- `game_server`: Entry point of the server application.
- `game_client`: Entry point of the simple client for testing application..

## How it Works

1. The server initializes and starts WebSocket listeners to handle incoming client connections.
2. Each connected client is assigned a dedicated actor to manage its communication and game state.
3. Game state is managed within the `game` package, ensuring thread-safe access using actors.
4. Clients send and receive messages through WebSockets, interacting with the game state through their assigned actors.

## Extending the Server

This project serves as a foundation for implementing various multiplayer game mechanics. You can extend it by:

- Adding new message types and handling them within the WebSocket and actor systems.
- Implementing different game mechanics within the `game` package.
- Enhancing the client-side code to accommodate new game features.

## Contributing

Contributions are welcome! If you find any issues or want to enhance the server's functionality, feel free to submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to customize this README to better suit your project and its specific details.
