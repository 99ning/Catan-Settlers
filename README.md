# Constructor

## Motivation
Constructor is a variant of the game settlers of Catan based on the information provided by University of Waterloo. This game was written in C++ and tested with valgrind as part of the CS246 final project (Fall 2020) at the University of Waterloo.

## Gameplay
This game supports exactly four players (builders) and allows them to build roads or residences in the given board by using five kinds of resources. Each player will gain building points when successfully build roads or residences. The first builder who has at least 10 building points will be the winner. Command is taken input via the command line and output is displayed via the command line.

## Available Commands
* **board**: prints the current board
* **status**: prints the current status of all builders in order from builder 0 to 3
* **residences**: prints the residences the current builder has currently completed
* **build-road <road#>**: attempts to builds the road at <road#>
* **build-res <housing#>**: attempts to builds a basement at <housing#>
* **improve <housing#>**: attempts to improve the residence at <housing#>
* **trade <colour> <give> <take>**: attempts to trade with builder <colour> giving one resource of type <give> and receiving one resource of type <take>
* **next**: passes control onto the next builder in the game. This ends the ”During the Turn” phase
* **save <file>**: saves the current game state to <file>
* **help**: prints out the list of commands

## Command line arguments
* **-seed xxx**: sets the random number generator’s seed to xxx. If you don’t set the seed, you always get the same random sequence every time you run the program.
* **-load xxx**: loads the game saved in file xxx. You may assume that the file being loaded was saved as a valid game state as described in the Saving section.
* **-board xxx**: loads the game with the board specified in the file xxx instead of using random generation. This file will contain the order of the tiles for the game as described in the saving the game section. The number of each tile present does not have to match
the random generation.
* **-random-board**: starts a game with a randomly generated board. If a game is being loaded, this command is ignored and the layout specified in the saved game is used instead.
