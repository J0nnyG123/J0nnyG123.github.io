# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> Generate[Generate Random Number]
    Generate --> Input[Get User Input]
    Input --> Validate{Is Input Valid?}
    Validate -- Yes --> Check[Check Guess]
    Validate -- No --> Error[Display Error Message]
    Error --> Input
    Check --> High{Is Guess High?}
    Check --> Low{Is Guess Low?}
    High -- Yes --> HighFeedback[Display "Too High!"]
    High -- No --> Low -- Yes --> LowFeedback[Display "Too Low!"]
    Low -- No --> Correct[Display "Correct!"]
    Correct --> End([End])
    HighFeedback --> Input
    LowFeedback --> Input

## description 
Start: The game begins.
Generate Random Number: A random number is selected within a specified range.
Get User Input: The user enters their guess.
Is Input Valid?: Check if the input is a valid number.
If Yes, proceed to check the guess.
If No, display an error message and prompt again.
Check Guess: Compare the guess to the random number.
Is Guess High?: If the guess is too high, display “Too High!” and prompt again.
Is Guess Low?: If the guess is too low, display “Too Low!” and prompt again.
Display “Correct!”: If the guess is correct, display a success message.
End: The game concludes.
