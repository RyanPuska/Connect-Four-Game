# Connect-Four-Game

In board.h:
We have a class called Board that has function declarations in public to display the board, run the game functionality, and check the win and tie status. The variable declarations are in private, used for the players' pieces, rows, columns, board array, and current player.

In board.cpp:
The Board constructor assigns each spot on the board with a "-" as soon as game starts. Then the displayBoard function displays the board each time it is called. After that, the choosePlace function is where most of the game logic lies. First we determine who's turn it is (Red always starts first). We prompt the user to enter a valid column number to place their piece. If the column choice is invalid or if the column is full, we prompt the user to try again. If valid, we call the checkWin and checkTie functions. The checkWin function checks all verticals, horizontals, and diagonals using for loops. If 4 identical pieces are found in a line, then the function returns true and we display the board and win message, and return to main. If it returns false, the checkTie function checks if every spot on the board is a red or yellow piece. If it is, then the function returns true and we display the board and tie message, and return to main. Otherwise, it returns false and it's the next user's turn. This choosePlace function repeats and displays the board after every move until checkWin or checkTie returns true.

In main.cpp: 
We create an object and call the displayBoard function, then call the choosePlace function. Once return 0 is reached, the program ends.
