# Python_Day_20
#Guess the Number Game: Build a game where the computer guesses a number chosen by the user
import random

def guess_the_number():
    print("Welcome to the Guess the Number Game!")
    print("Think of a number between 1 and 100, and I'll try to guess it.")

    low = 1
    high = 100
    attempts = 0

    while True:
        guess = random.randint(low, high)
        attempts += 1
        print(f"My guess is: {guess}")

        feedback = input("Is it too high (H), too low (L), or correct (C)? ").upper()
        
        if feedback == 'C':
            print(f"Yay! I guessed your number {guess} in {attempts} attempts!")
            break
        elif feedback == 'H':
            high = guess - 1
        elif feedback == 'L':
            low = guess + 1
        else:
            print("Invalid input. Please enter H, L, or C.")

# Run the game
guess_the_number()
