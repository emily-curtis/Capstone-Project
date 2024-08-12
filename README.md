This project simulates the classic Hangman game, where the player tries to guess a hidden word one letter at a time. 
The hidden words in this simulation are randomly selected from a list of nouns stored in an external file, englishnouns.txt. 
The computer selects a random word from a text file containing the top 1000 most common words in the English language, and the user subsequently must attempt to guess the word, letter by letter. 
If the user guesses incorrectly, the hangman gets closer to death. 
The user therefore must try and guess the correct word before the hangman is fully dead, at which point they lose the game. If they guess the word correctly, then they win.


**Variables**

*computer_word* is the randomly selected word from the txt file. 
*blank_word* is the correctly guessed letters in computer_word. This starts off ‘blank’ and is represented by underscores to start with.
*user_letter* is the letter guessed by the user on that specific turn. This changes each time as the user guesses a new letter, which is then stored in this variable.
*guess_count* is the number of guesses that the user has made thus far, and is used to create the hangman graphic when the user guesses incorrectly.
*guess_letters* is a list which stores all of the unique letters that the user has guessed so far. If the user guesses a repeat letter, or a word, this will not be stored in this variable.
*user_choice* is the variable used at the end of the game to determine if the user would like to play again, or exit the game.


**Functions**

*random_word()* is the function that consults the txt file and assigns a random word to the variable computer_word. It then creates the blank_word variable based on the length of the chosen random word.
*edit_blank()* is the function that inserts the correctly guessed letter in the correct index in the blank word, so that it matches the index of that letter in the computer word.
*hangman_graphic()* takes the guess_count as an input and uses this to determine which hangman graphic should be printed to the console.
*user_guess()* is the function that checks that the blank_word variable is not yet the same as the computer_word  variable and then calls the no_repeats function to take the user guess. 
This function then adds the user guess to the guess_count variable and then informs the user of whether their guess was correct or incorrect. If the guess was incorrect, the function displays a hangman graphic, and adds 1 to the guess_count total. 
*no_repeats()* is the function that asks the user for their guess, and then checks that the user guess is not a repeat and that the guess is a single letter (not a blank space or a word).
*you_lost()* is the function that checks the guess count of the user and informs them that they either won, lost, or if the guess count is lower than 6, then the function simply prints out the letter that they have guessed so far. 
*play_again()* is the function that takes a user input (y or n) to the question ‘would you like to play again?’. If the user would like to play again, the game starts again. If not, the game exits. 
