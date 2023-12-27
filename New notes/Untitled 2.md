# Prequsitories
To run this file you will need Linux distribution. Any modern release will work from Debian however for this project I have used Linux distribution in **WLS** `kali-linux 2023.4`. To compile file I have used g++ version `Debian 13.2.0-5`. It should work with most of the distributions including popular ones such as **Ubuntu or Debian**.

# How to run a file
Please navigate to the directory where the project is stored in the terminal.
![[Pasted image 20231227231725.png]]
By using command `cd` navigate to the project directory and type `./tictactoe`. This will run the **tic tac toe** game. If the file doesn't exist you will need to compile it with **g++** by typing this command first in the directory the project is stored in `assigment-2023-tictactoe`.
```Shell
g++ -o tictactoe tic_tac_toe.cpp
```
```Shell
./tictactoe
```

![[Pasted image 20231227231950.png]]

## Games Rules
Game if fairly simple to play. You