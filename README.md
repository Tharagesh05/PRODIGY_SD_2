# PRODIGY_SD_2//
Code for a Guessing Game//
import random

def guessing_game():
    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guessed_correctly = False
    
    print("Welcome to the Number Guessing Game!")
    print("I have selected a number between 1 and 100. Try to guess it!")
    
    while not guessed_correctly:
        # Get user's guess
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            # Compare the guess with the generated number
            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                guessed_correctly = True
                print(f"Congratulations! You've guessed the correct number {number_to_guess} in {attempts} attempts.")
        except ValueError:
            print("Please enter a valid number.")
    
if __name__ == "__main__":
    guessing_game()

