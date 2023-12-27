# Prerequisites
To run this file you will need Linux distribution. Any modern release will work from Debian however for this project I have used Linux distribution in **WLS** `kali-linux 2023.4`. To compile file I have used g++ version `Debian 13.2.0-5`. It should work with most of the distributions including popular ones such as **Ubuntu or Debian**.
![[Pasted image 20231227231725.png]]

## G++ & Git Installation
With some distribution `g++` tool is not installed by default. To install g++ please use following command in your Linux terminal *(Debian based)*:
```Shell
sudo apt install g++
```
If for some reason the installation hasn't succeeded it's because OS needs an update. Please type this command before the one above.
```Shell
sudo apt update && sudo apt upgrade
```
![[Pasted image 20231227233438.png]]

Also `Git` may not be installed. Similarly to g++ run this command to install git:
```Shell
sudo apt install git
```
![[Pasted image 20231227235612.png]]

# How to run a tic tac toe game
First clone the project by running this command
```shell
git clone https://gitlab.uwe.ac.uk/l2-pazdro/assigment-2023-tictactoe
```

Please navigate to the directory where the project is stored via the terminal.
![[Pasted image 20231227233723.png]]
By using command `cd` navigate to the project directory and type `./tictactoe`. This will run the **tic tac toe** game. If the file doesn't exist you will need to compile it with **g++** by typing this command first in the directory the project is stored in `assigment-2023-tictactoe`.
```Shell
g++ -o tictactoe tic_tac_toe.cpp
```
```Shell
./tictactoe
```

![[Pasted image 20231227231950.png]]

## Games Rules & How to play
Game if fairly simple to play. Players are labelled `X` or `O` and each turn they are switched. The purpose of the game is for one of the players to get their symbols 3 horizontally or vertically, or diagonally. Player needs to select number between 1-9. Game should print board numbers grid that corresponds with the main board.

- Example game 1 **(O Wins)**:
![[Pasted image 20231227233926.png]]

Game is capable of understanding different inputs from the players just in case they make mistake
- Example game 2 **(X makes a mistake)**:
![[Pasted image 20231227234154.png]]
X tried to type 1 which is already occupied which throws and error and asks player to type different input (number).

Game can also be draw if nobody wins:
- Example game 3 **(Draw)**:
![[Pasted image 20231227234649.png]]

### Additional info
- Colours may differ depending on colour palette used by the terminal
- Games has been tested for various inputs and only accepts the numbers or "stop" string
-