Real-Time Chess Game
A real-time multiplayer chess game built with Node.js, Express, Socket.io, and Chess.js. Players can join as white or black pieces, with additional users joining as spectators.

🚀 Features

Real-time Multiplayer: Two players can play against each other in real-time.
Spectator Mode: Additional users can watch the game as spectators.
Drag & Drop Interface: Intuitive piece movement with drag and drop.
Move Validation: Server-side move validation using Chess.js.
Role Assignment: Automatic assignment of white/black roles to players.
Responsive Design: Clean, modern UI with Tailwind CSS.

🛠 Technologies Used

Backend:

Node.js
Express.js
Socket.io
Chess.js (for game logic and move validation)
EJS (templating engine)


Frontend:

HTML5
CSS3
JavaScript (ES6+)
Socket.io Client
Tailwind CSS


Additional:

Web3 integration (planned/in development)



📋 Prerequisites
Before running this project, make sure you have:

Node.js (v14 or higher)
npm or yarn package manager

🔧 Installation

Clone the repository
bash
git clone <your-repository-url>
cd chess-game

Install dependencies
bash
npm install

Required packages
bash
npm install express socket.io chess.js ejs


🚀 Getting Started

Start the server
bash
node app.js

Open your browser
Navigate to http://localhost:3000

Start playing

First player gets white pieces.
Second player gets black pieces.
Additional users become spectators.



📁 Project Structure
chess-game/
│
├── app.js                 # Main server file
├── public/
│   └── js/
│       └── chessGame.js   # Client-side game logic
├── views/
│   └── index.ejs          # Main game template
└── package.json
🎮 How to Play

Join Game: Open the application in your browser
Player Assignment:

First player automatically becomes White.
Second player automatically becomes Black.
Additional users become spectators.


Move Pieces: Click and drag pieces to make moves.
Game Rules: Standard chess rules apply with server-side validation.

🔄 Game Flow

Players connect via Socket.io.
Server assigns roles (white/black/spectator).
Players make moves using drag & drop.
Moves are validated server-side using Chess.js.
Valid moves are broadcasted to all connected clients.
Board state is synchronized across all clients.

🤝 Contributing

Fork the repository.
Create a feature branch (git checkout -b feature/AmazingFeature).
Commit your changes (git commit -m 'Add some AmazingFeature').
Push to the branch (git push origin feature/AmazingFeature).
Open a Pull Request.

🆘 Troubleshooting
Common Issues:
Pieces not displaying:

Check if getPieceUnicode() function is implemented.
Verify piece symbols are properly set.

Moves not working:

Ensure handleMove() function is implemented.
Check socket connections in browser console.

Styling issues:

Verify Tailwind CSS is loading properly.
Check CSS selectors for typos.

📞 Support
If you encounter any issues or have questions:

Check the console for error messages.
Verify all dependencies are installed.
Ensure port 3000 is available.
Check socket.io connection status.


Happy Gaming! 🎯♟️
