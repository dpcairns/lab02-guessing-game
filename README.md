# Guess a number App

## HTML Setup
1) Number Input
    - Why? So the user can enter their guesses
2) Button
    - Why? To submit the guess and trigger state changes
3) Guesses remaining span
    - Why? To display remaining guesses
4) (Too high/Too low/You got it!) span
    - Why? Tell the user what's wrong with their guess (if anything)
*5) Reset button

1) Go grab these DOM elements (that means they need ids!)
2) Initialize state (our global `let`s)
    - Random number: n
    - Guesses remaining: 4
3) Add event listener to button
    - On click
        1) STATE: decrement remaining guesses by 1 (--)
        2) Store user guess in a variable (`Number(someInput.value)`)
        3) Compare user guess with random number
        4) VIEW:
            a) if user guess is greater than the random number, inject 'too high' into our results span
                - VIEW: check if there are any guesses left. If not, disable the input and add a losing message
            b) if user guess is less than the random number, inject 'too low' into our results span
                - VIEW: check if there are any guesses left. If not, disable the input and add a losing message
            c) if the user guess is equal to the random number, congratulate the user.
                - disable the input and display a winning message
        5) VIEW: If applicable, Change the remaining guesses text content
4) **STRETCH** Add an event listener onto the reset button
    - On click
        1) STATE: Reset remaining guesses state to 4
        2) STATE: Create a new random number
        3) VIEW: re-enable the inputs if they are disabled and fix the game text