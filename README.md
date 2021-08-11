# Dice-Rolling-Simulator

import random

def welcome_message():
    print("Welcome to the dice rolling simulation!")
welcome_message()

exit_wanted = 1

def dice(number_of_rolls):
    roll_count = 0
    while roll_count < number_of_rolls:
        throw = random.randint(1,6)
        print("You got", throw)
        number_of_rolls -= 1
        print(number_of_rolls, "rolls left.")


while exit_wanted != 0:
    dice(int(input("How many times would you like to roll the dice?\n")))

    play_again = input("Do want to play again?\n").lower()
    if play_again == "no":
        exit_wanted = 0
