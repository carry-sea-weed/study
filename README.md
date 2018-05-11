"# study" 
# Guess My Number Reverse Version
#
# game introduction
print("Imagine one number between 1 and 100. Don't forget it!")
print("The number computer provide is your number.")
print("If it is lower than yours, press 'l'.")
print("If it is higher than yours, press 'h'.")
print("If it is the same as yours, press 'c'")
print("Then, press the enter key.")

# set name
lowest = 0
highest = 101

# guess
import random

guess = random.randint(lowest+1,highest-1)
print("Your number is",guess,"? ")

# input
reply = input("Tell me, l or h or c? ")

# condition
while reply != "c":
    if reply == "l":
       lowest = guess

    elif reply == "h":
        highest = guess
    else:
        print("?")

    if lowest+1 >= highest-1:
        print("ERROR!")
        break
    guess = random.randint(lowest+1,highest-1)
    print("Your number is",guess,"?")
    reply = input("Tell me, l or h or c? ")

if reply == "c":
    print("I see! Your number is",guess,". Thank you very much.")