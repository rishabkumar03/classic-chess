# Real-Time Chess Game

A real-time multiplayer chess game built with Node.js, Express, Socket.io, and Chess.js. Players can join as white or black pieces, with additional users joining as spectators.

## Features

- **Real-time Multiplayer**: Two players can play against each other in real-time.
- **Spectator Mode**: Additional users can watch the game as spectators.
- **Drag & Drop Interface**: Intuitive piece movement with drag and drop.
- **Move Validation**: Server-side move validation using Chess.js.
- **Role Assignment**: Automatic assignment of white/black roles to players.
- **Responsive Design**: Clean, modern UI with Tailwind CSS.

## Technologies Used

- **Backend**: Node.js, Express.js, Socket.IO, Chess.js
- **Frontend**: HTML5, CSS3, JavaScript (ES6+), Socket.IO Client, Tailwind CSS
- **Template Engine**: EJS
- **Game Logic**: Chess.js for rules and move validation
- **Planned Features**: Web3 integration

## Prerequisites

Before running this project, make sure you have:
- Node.js (v14 or higher)
- npm or yarn package manager

## Installation

1. Clone the repository:
   ```bash
   git clone <your-repository-url>
   cd chess-game
   ```

2. Install the required dependencies:
   ```bash
   npm install
   ```

3. (Optional) Manually install required packages if needed:
   ```bash
   npm install express socket.io chess.js ejs
   ```

## Usage

1. Start the server:
   ```bash
   node app.js
   ```
   
2. Open your web browser and navigate to:
   ```arduino
   http://localhost:3000
   ```
   
3. Game roles are assigned automatically:
- First player to join becomes White
- Second player becomes Black
- All others join as Spectators

4. Play the game:
- Drag and drop pieces to make moves
- All moves are validated server-side

## File Structure
```
classic-chess/
├── app.js              # Main server file
├── public/
│   └── js/
│       └── chessGame.js # Client-side game logic
├── views/
│   └── index.ejs       # Main HTML template
└── package.json        # Project dependencies and scripts
```

## How It Works

1. **Client Connection**: Players or spectators connect via Socket.IO
2. **Role Assignment**: The first player is assigned White, the second is Black, others are Spectators
3. **Move Handling**: Players make moves via drag & drop
4. **Move Validation**: The server validates moves using Chess.js
5. **Broadcasting**: Valid moves are broadcasted to all connected clients
6. **State Sync**: Board state is kept synchronized across all devices

## Configuration

### Port Configuration

The application runs on port 3000 by default. You can change this in app.js:
```javascript
server.listen(3000); // Change to your desired port
```

## Known Issues

1. **Pieces Not Displaying**: Check getPieceUnicode() function and piece symbol mappings
2. **Moves Not Working**: Ensure handleMove() is implemented and Socket.IO is connected
3. **Styling Issues**: Verify Tailwind CSS is properly loaded and CSS selectors are correct

## Troubleshooting

### Pieces Not Displaying

- Confirm that getPieceUnicode() returns correct symbols
- Verify piece images/symbols are correctly linked

### Moves Not Working
- Ensure handleMove() function is implemented correctly
- Check socket connection in the browser console

### Styling Issues
- Verify Tailwind CSS is loading properly
- Ensure no typos in class names or CSS selectors

## Security Considerations

- Game Integrity: All move validation is done server-side to prevent cheating
- HTTPS: Use HTTPS in production for secure communication
- Rate Limiting: Implement rate limiting to prevent flooding
- Authentication: Consider adding authentication for private matches

## Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

**Happy Gaming! 🎯♟️**
