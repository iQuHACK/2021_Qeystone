# Bit Battle

## Abstract:

Understanding gates on qubits is essential to working with quantum computers. This game aims to educate people on the basic gates that are commonly used and how they manipulate states. The game is one player, against the computer. Both players have access to one qubit, and are trying to place it in either the zero or one state by applying gates so the probability is in their favor. A quantum measurement is then performed on real hardware, determining the winner.

## How To Play:

Setting Up Dependencies

- Package requirements: python-dotenv, jupylet
- Jupylet is not compatible with Python 3.9.

Pip install the packages above.

- Run the following for Python 3.8 on Windows: python -m jupylet postinstall

Gameplay

- The game is a jupyter notebook: `bitbattle.ipynb`. Run this to play.
- The objective of the game is to get the highest probability of getting the game qubit to be measured as state |1>. If the state measures to |0>, then you lose the game. 
- At the beginning of the game, you will have a hand of 8 cards. You may play a card per turn. Each card manipulates the state of the qubit. However, for each card you use, you must wait a specific number of turns again to use it.

## Development process:

- First, the basic gameplay had to be developed, structuring the game.
- The game UI was created using Jupylet, a Jupyter-friendly version of Pyglet from OpenGL. A shell was created in order to ensure communication between moves was functional before quantum computations were factored into the code.
- Then code to work with the backend was created: measurements are run on real Quantum Hardware in a measurement function per turn, to tell the players who’s currently winning. One final measurement at the end determines the winner of the match.

## Possible extensions/future work:

- The game can be made more complex with multiple qubits, enabling entanglement and other more complicated behavior. 
- Grover’s search algorithm takes an equally superimposed state and brings it closer and closer to a desired state. This concept could possibly be applied in the multiple qubit game, with both players working against each other to “search” for the state they are looking for.