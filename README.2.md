<!-- 1. Importing Required Modules -->
random: Used for shuffling the colors list.
tkinter: The main module for creating the GUI.
messagebox: (Commented out) Used for displaying messages to the user.


<!-- 2. Global Variables -->
colours: A list of color names.
score: Initialized to 0, keeps track of the user's score.
timeleft: Initialized to 30, represents the time left in the game.


<!-- 3. Function Definitions -->
next_colour()
Purpose: Updates the game state by changing the displayed color and checking the user's guess.

Steps:
Checks if the game is still in progress.
Gets the user's input and compares it with the correct color.
Updates the score if the guess is correct.
Clears the input field.
Randomly shuffles the colors list.
Updates the displayed color and score label.
countdown()
Purpose: Decreases the time left by 1 every second until it reaches 0.

Steps:
Checks if the game is still in progress.
Decreases the time left by 1.
Updates the time left label.
Calls itself after 1000 milliseconds (1 second) to continue the countdown.
Calls scoreshow() when the time runs out.
record_highest_score()
Purpose: Records the highest score achieved in the game.

Steps:
Calls load_highest_score() to get the current highest score.
If the current score is higher, writes the new score to a file.
load_highest_score()
Purpose: Loads the highest score from a file.

Steps:
Tries to open the file containing the highest score.
Returns the score if found, or 0 if the file does not exist.
scoreshow()
Purpose: Displays the highest score in a new window.

Steps:
Calls record_highest_score() to ensure the highest score is recorded.
Creates a new window.
Displays the highest score in the new window.
start_game(event)
Purpose: Starts the game when the Enter key is pressed.

Steps:
Checks if the game is starting for the first time.
Starts the countdown.
Calls next_colour() to display the first color.


<!-- 4. GUI Setup -->
Window Creation: Creates the main window for the game.
Widget Creation: Creates and packs various labels and an entry widget for user input.
Event Binding: Binds the Enter key to the start_game function.
Main Loop: Starts the Tkinter event loop to run the application.


<!-- 5. Game Flow -->
Starting the Game: The user presses Enter to start the game.
Playing the Game: The user guesses the color of the text displayed.
Ending the Game: The game ends when the time runs out.
Displaying the Score: The user's highest score is displayed in a new window.