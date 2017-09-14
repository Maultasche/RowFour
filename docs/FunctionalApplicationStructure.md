# Functional Application Structure

Here we outline the application flow and what functionality is available.

1. The application starts up at the beginning of a game at the first turn for Player 1
2. When a player turn begins, the current state of the board is output with numbers above each column. Below that, we output whose turn it is as part of the command prompt and let the player type in a command. During the first turn, the player is also prompted to enter their choice or type ? for a list of options
	1. The ? lists the player choices and then returns to the input prompted
	2. The player choices
		1. "1" to "X", where X is the number of columns (not to exceed 9): drops a token in a column
		2. "?": lists the player choices
		3. "d": display the game board
		4. "q": quit the game
		5. "r": restart the game
	3. An attempt to play a column that doesn't exist will display an appropriate message on its own line and the prompt will reappear on the line below that
	4. An attempt to play a column that is full of tokens will display an appropriate message on its own line and the prompt will reappear on the line below that
	5. Displaying the board will cause the board to be output and the prompt will display below that
	6. Quitting the game will exit the program entirely
	7. Restarting the game will cause the first turn of a new game to be displayed, as if the application had just been started
	8. Typing anything else will cause a message to be displayed that indicates that the command is not recognized, and that typing in "?" will cause the player choices to be displayed
3. When a player wins or there is no winner after the board has been filled up, an appropriate message is displayed, and a prompt appears below that. Instead of listing the player's turn, the prompt indicates that the player whould press "q" to quite or "r" to restart with a new game.
	1. "q", "r", "d", and "?" are the only valid options at this point
	2. "q", "r" behave as they normally would
	3. The "d" option will display the final prompt again after the board is redrawn
	4. The "?" option will only display the options that are valid at this point

