

# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateRandomNumber[Generate Random Number]
    GenerateRandomNumber --> UserInput[Prompt User for Guess]
    UserInput --> ValidateInput{Is Input Valid?}
    ValidateInput -->|Yes| CheckGuess[Check Guess]
    ValidateInput -->|No| InvalidInput[Prompt for Valid Input] --> UserInput
    CheckGuess -->|Correct| Success[Display Success Message] --> End([End])
    CheckGuess -->|Too High| HighGuess[Display "Too High!"] --> UserInput
    CheckGuess -->|Too Low| LowGuess[Display "Too Low!"] --> UserInput
    End[[End]]
    ```

Start: Initiates the guessing game.
Generate Random Number: The program generates a random number within a specified range (e.g., 1 to 100).
Prompt User for Guess: The user is asked to input their guess for the random number.
Is Input Valid?: The program checks if the input is a number and falls within the allowed range:
Yes: If the input is valid, the program proceeds to check the user's guess.
No: If the input is invalid (e.g., non-numeric input or out of range), the program prompts the user to enter a valid guess and loops back to the user input step.
Check Guess: The program evaluates the user's guess:
Correct: If the guess matches the random number, the program displays a success message and concludes the game.
Too High: If the guess is greater than the random number, the program notifies the user that their guess was too high and asks for another guess.
Too Low: If the guess is less than the random number, the program notifies the user that their guess was too low and asks for another guess.
End: The game concludes after the user successfully guesses the correct number.
