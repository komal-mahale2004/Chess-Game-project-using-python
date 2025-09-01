Chess-Game-project-using-python
# overview
The Chess Game is a Python-based application that allows two players to play chess interactively.
It uses object-oriented programming to define pieces, rules, and moves, while providing a GUI board built with Tkinter/Pygame.

<img width="1441" height="1017" alt="image" src="https://github.com/user-attachments/assets/790e5e72-65d0-4bb5-ae5d-d0f8ff16e6f2" />

This project is a great way to learn game development, GUI programming, and algorithm design in Python.

#🚀 Features
🎮 Play two-player chess on a GUI board.
✅ Enforces legal chess moves (pawn, rook, knight, bishop, queen, king).
👑 Detects check & checkmate conditions.
🖥️ Graphical interface using Tkinter/Pygame.
🎓 Beginner-friendly example of OOP + game logic.
🛠️ Tech Stack
#Language: Python
Libraries: Tkinter / Pygame
Concepts: Object-Oriented Programming, Game Loops, Event Handling
📂 Project Structure
project/ │── chess.py # Main game logic │── pieces.py # Chess piece classes (Pawn, Rook, etc.) │── gui.py # GUI code (Tkinter/Pygame) │── assets/ # Piece images (PNG) │── README.md

#▶️ Usage
Run the chess game with:

python chess.py


Select and move pieces using mouse clicks.

Game enforces legal moves and alternating turns.

📸 Example Screenshot

(Insert screenshot of chessboard here)

🔮 Future Enhancements

🤖 Add AI opponent using Minimax algorithm.

⏱️ Add timer & move history log.

🌍 Enable online multiplayer mode.

🎨 Improve UI with better graphics.

📜 License

This project is licensed under the MIT License – free to use and modify.


---

## 🔹 Sample Python Code (Simplified Version – Tkinter)  
```python
import tkinter as tk

# Board dimensions
BOARD_SIZE = 8
TILE_SIZE = 60

root = tk.Tk()
root.title("Chess Game")

canvas = tk.Canvas(root, width=BOARD_SIZE*TILE_SIZE, height=BOARD_SIZE*TILE_SIZE)
canvas.pack()

# Draw chess board
for row in range(BOARD_SIZE):
    for col in range(BOARD_SIZE):
        color = "white" if (row+col) % 2 == 0 else "gray"
        canvas.create_rectangle(col*TILE_SIZE, row*TILE_SIZE,
                                (col+1)*TILE_SIZE, (row+1)*TILE_SIZE, fill=color)

# Place sample pieces (use text instead of images for simplicity)
pieces = {"R": (0,0), "N": (0,1), "B": (0,2), "Q": (0,3), "K": (0,4)}
for p, (row,col) in pieces.items():
    canvas.create_text(col*TILE_SIZE+30, row*TILE_SIZE+30, text=p, font=("Arial", 24))

root.mainloop()

