# Tic Tac Toe Game with Minimax Algorithm

Welcome to the Tic Tac Toe game featuring a challenging AI opponent powered by the Minimax algorithm. This README will guide you through setting up and playing the game.

## Overview

This project is a command-line implementation of Tic Tac Toe, where you can play either against a friend or against a computer opponent that uses the Minimax algorithm to ensure optimal play.

## Features

- **Single-player mode**: Play against a computer that uses the Minimax algorithm.
- **Multi-player mode**: Two players can play against each other on the same device.
- **Simple interface**: A text-based interface that is easy to use.

## Getting Started

### Prerequisites

- Python 3.x

### Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/Anjana2002/Tic_Tac_Toe.git

    ```


### Running the Game

To start the game, run the following command:

```bash
python Tic_Tac_Toe.py
```
How to Play
In single-player mode, the computer (O) plays against the player (X). The player can choose to go first or second.
In multi-player mode, two players take turns. Player 1 is X, and Player 2 is O.
The board positions are numbered 1 to 9 as follows:
```bash
1 | 2 | 3  
4 | 5 | 6  
7 | 8 | 9
 ```
To place your mark on the board, enter the position number.

The game continues until there is a winner or the board is full (a draw).

Minimax Algorithm
The Minimax algorithm is used by the computer to determine its moves. Here's how it works:

Maximizing and Minimizing: The algorithm treats the computer as the minimizing player and the human as the maximizing player.
Recursive Search: It explores all possible moves, simulating future states of the game.
Score Evaluation: It assigns scores to game outcomes: +1 for a win, -1 for a loss, and 0 for a draw.
Optimal Move Selection: It selects the move with the highest score for the computer.
Code Structure
The main script containing the game logic and the Minimax algorithm implementation can be found in Tic_Tac_Toe.py.

Example Code
Here is a snippet of the Minimax function used in the game:

python
```bash
def minmax(board, player):
    winner = analyseboard(board)
    if winner != 0:
        return winner * player
    value = -2
    pos = -1
    for i in range(9):
        if board[i] == 0:
            board[i] = player
            score = -minmax(board, -player)
            board[i] = 0
            if score > value:
                value = score
                pos = i
    if pos == -1:
        return 0
    return value
```
Enjoy playing Tic Tac Toe!
