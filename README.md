## Project description
The is problem 14 from the final projects list for summer 2023. Here is the description of the game:

*There are two players, A and B. At the beginning of the game, each starts with 4 coins, and there are 2 coins in the pot. A goes first, then B, then A, and so on. During a particular player’s turn, the player tosses a 6-sided die. If the player rolls a:
1, then the player does nothing.
2: then the player takes all coins in the pot.
3: then the player takes half of the coins in the pot (rounded down).
4,5,6: then the player puts a coin in the pot.*

*A player loses (and the game is over) if they are unable to perform the task (i.e., if they have 0 coins and need to place one in the pot). We define a cycle as A and then B completing their turns. The exception is if a player goes out; that is the final cycle (but it still counts as the last cycle). We are trying to determine the expected number (and maybe even the distribution) of cycles the game will last for. I’m guessing that you can use “first-step” analysis to get the expected value. Simulation seems the easiest thing to do to get the entire distribution.*


The game is stored in `game.py` and "first-step" analysis is provided in the notebook `analysis.ipynb`.

## Code 
1. game.py - game definition for Monte Carlo simulation
2. markov_chain_game.py - Markov chain implementain to get to steady state probabilities.
3. analysis.ipynb - Jupyter notebook has Monte Carlo and Markov Chain runs and tries to approximate the Monte Carlo runs.

## Running the Code:
### Setting up the enviornment
The `environment.yaml` file contains the setup for the enivronment. It can be created using:
```
conda env create --file environment.yaml
```
You may need to install the fitter package, using `pip install fitter`.

Ensure the all the files are in the same directory

### Running
Just run the notebook `analysis.ipynb`. It is divided into two sections.
- Section 1: Uses the `game.py` file to run Monte Carlo simulations (**Note:** You can skip the subsection wiht 10,000,000 trials, since that will take a lot of time to run)
- Section 2: Uses the `markov_chain_game.py` file to get the exact distribution in Section 2.


## Python packages and version

For reference, here are the python packages and their versions used:
Python              3.11.2
fitter              1.5.2
matplotlib          3.7.1
matplotlib-inline   0.1.6
pandas              1.5.3
plotly              5.13.1
scikit-learn        1.2.1
scipy               1.10.1
seaborn             0.12.2
statsmodels         0.14.0
