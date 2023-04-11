# python-guess_the_number.py
#In this project, you will create a game that generates a random number and asks the player to guess it. The game will continue until the player correctly guesses the number.
import random

number = random.randint(1, 100)
guess = 0
count = 0

print("Guess the number between 1 and 100!")

while guess != number:
    guess = int(input("Enter your guess: "))
    count += 1
    
    if guess < number:
        print("Too low! Guess again.")
    elif guess > number:
        print("Too high! Guess again.")
    else:
        print("You got it! The number was", number)
        print("It took you", count, "tries to guess the number.")
