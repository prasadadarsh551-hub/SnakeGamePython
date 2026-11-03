
🐍 Snake Game (PS No. 35)

A console-based Snake Game simulation written in Python 3. Instead of using live keyboard input, the player types a sequence of moves, and the program plays them out one by one on a 10 × 10 grid, reporting the snake's head position, food eaten, score, and whether the game ends.

📖 About the Project

Snake is a classic arcade game in which a snake moves around a grid, eats food to grow longer, and must avoid hitting the walls or its own body. This project recreates that logic in plain Python as a step-by-step simulation.

Rather than reading live key presses, the program takes a list of moves (R, L, U, D) from the user and plays them out in order on a 10 × 10 grid. After each move it shows where the snake's head is, and it announces when food is eaten, how the score and length change, and when the game is over.

The goal of the project is to practise core Python fundamentals — lists, tuples, dictionaries, loops and conditions — while building a small but complete game with scoring, input validation and collision detection.

📋 Project Details

Field	Details

PS Number	35

Project Title	Snake Game

Student Name:	Adarsh Kumar Prasad

ERP ID:	RU-26-02948

Email:	adarsh.prasad@rungta.org

Section:	BTECH (CSE) B2

🎯 Features

10 × 10 grid with coordinates from (0, 0) to (9, 9)
Snake starts at (5, 5) and initially faces Right
Predefined food positions: (7, 5) first, then (0, 0)
+10 points for every food eaten, and the snake grows by 1
Input validation: only R, L, U, D are accepted
Reverse moves are blocked (the snake cannot turn back onto itself directly)
Wall collision detection ends the game
Self collision detection ends the game
Case-insensitive input and extra spaces are handled automatically

🧠 Concepts Used

Lists and tuples (snake body and coordinates)
Dictionaries (mapping keys to directions)
Loops and conditional statements
String handling (upper(), split(), strip())
Basic game logic: collision detection and scoring
⚙️ Requirements
Python 3.x (no external libraries needed)

Check your version:

bash
python --version

▶️ How to Run

Save the program as snake_game.py.
Open a terminal in the same folder.
Run:
bash
python snake_game.py
When prompted, enter your moves separated by commas:
Moves: R,R,D,L

🎮 Controls

Key	Direction	Change in (x, y)
R	Right	(+1, 0)
L	Left	(−1, 0)
U	Up	(0, −1)
D	Down	(0, +1)

🧪 Sample Runs

Eating the first food

Moves: R,R
Head: (6, 5)
Food eaten at (7, 5) !
Score: 10 | Length: 2 | Head: (7, 5)

Invalid key

Moves: R,X,R
Head: (6, 5)
Invalid key. Use R, L, U or D.
Food eaten at (7, 5) !
Score: 10 | Length: 2 | Head: (7, 5)

Reverse move blocked, then wall hit

Moves: L,U,U,U,U,U,U
Reverse move not allowed. Snake continues Right.
Head: (5, 4)
Head: (5, 3)
Head: (5, 2)
Head: (5, 1)
Head: (5, 0)
Game Over! Wall hit at (5, -1)
Final score: 0

Full output are in testcase.pdf.

🔍 How It Works

The snake is stored as a list of (x, y) tuples, with the head at index 0.
The user's input is split into individual moves and processed in order.
For each valid move, a new head position is calculated.
If the new head is outside the 0–9 range, the game ends (wall hit).
If the new head matches the food, the snake grows and the score increases by 10.
Otherwise the snake moves forward: a new head is added and the tail is removed, after checking that the head does not hit the body.
When the moves finish (or the game ends), the final result is printed.

📁 Project Structure

snake-game/

├── snake_game.py

└── README.md

🚀 Possible Improvements

Randomly generated food positions
Live keyboard controls using a library such as Pygame
A visual grid printed after every move
A high-score system

👨‍🏫 Project Mentor

Mentored by: Mr. Satyaprakash Sethy

GitHub: @SARYAPRAKASHSETHY

Role: Python Mentor / Technical Guide
