# Pythonproject-escapethemanor
Escape the manor project

#variables
health = 100
amountofpuzzlescompleted = 0
amountofpuzzles_total = 7
backpack = []

import tkinter as tk

window = tk.Tk()
window.title("Escape the Manor")
window.geometry("500x300")

label = tk.Label(window, text="Welcome to the manor!")
label.pack(pady=20)

window.mainloop()

def open_new_window():
   new_window = tk.Toplevel(window)
   new_window.title("New Window")
   new_window.geometry("300x200")

button = tk.Button(window, text="Open New Window", command=open_new_window)
button.pack()

def lose_health(amount):
   global health
   health = max(0, health - amount)

#intro
print("On Halloween night you are walking home on the side of the road, when suddenly you are grabbed by a guy in a van. They take you to a manor in your town that is known to be haunted by all the locals and have the doors locked from the outside. You now have two hours to solve seven puzzles before you become one of the ghosts that reside in the manor.")

#puzzle_1
print("You enter the manor")
print("Puzzle 1: You and your sister (5) re different ages. you are twice her age at 16. how old is your sister when your 45?")
print("2   2")
print("  -  ")
print(" --- ")


print("Your answer:")
answer = input()
if answer == "37":
   print("Correct!")
   amountofpuzzlescompleted += 1
   print("You have completed " + str(amountofpuzzlescompleted) + " out of " + str(amountofpuzzles_total) + " puzzles.")
else:
   lose_health(25)
   print("Incorrect! The correct answer is 37. You are twice your sister's age at 16, which means she is 8 years old. When you are 45, she will be 45 - 8 = 37 years old.")
   print("you lost health! You have " + str(health) + " health left.")

#puzzle_2

def puzzle_2():
   global health, amountofpuzzlescompleted  # noqa: PLW0602

print("      7777777      ")
print("    77       77    ")
print("   77   7 7   77   ")
print("   77         77   ")
print("   7777777777777   ")
print("   77 77 77 77 77   ")
print("   77 77 77 77 77   ")
print("      77   77      ")
  
  
print("The(2)e are 3 people: Tori, Ralph, and John.")
print("One is an engineer, one is an electrician, and one is a plumber.")
print("Ralph is not an engineer or a plumber.")
print("John is an electrician or a plumber.")
print("Tori is not a plumber.")

answer = input("Who is the engineer? ").strip().lower()
if answer == "tori":
       print("Correct! Tori is the engineer.")
       amountofpuzzlescompleted += 1
       print("You have completed " + str(amountofpuzzlescompleted) + " out of " + str(amountofpuzzles_total) + " puzzles.")
else:
       lose_health(25)
       print("Incorrect! Ralph is the electrician, John is the plumber, and Tori is the engineer.")
       print("You lost health! You have " + str(health) + " health left.")

#puzzle_3
print("The user will have to solve an equation that comes from the 2 logic puzzles. It will show an equation with 2 variables, both variables values are shown somewhere in the text for both of the first logic puzzles shown above.")

print("3333333333333")
print("3  .    .   3")
print("3 3 3 3 3 3 3")
print("3           3")
print("3    ----   3")
print("3333333333333")
print("3 3 3 3 3 3 3")
print("3   3   3   3")
print("3   3   3   3")


print("Puzzle 3: Solve the equation")
print("5y(3x-y)^x")

x = 2
y = 5

correct_answer = 5 * y * (3 * x - y) ** x

answer = input("Enter your answer: ")

if answer.strip() == str(correct_answer):
   print("Correct! You solved Puzzle 3!")
else:
   print("Incorrect! The correct answer is 25.")

print("x = 2 and y = 5")

#Functions:
def puzzle_4():
   global health, amountofpuzzlescompleted  # noqa: PLW0602
  
   input_puzzle_4 = input("\nWhat are the two most important letters for a couple, until they break up?\nPut an 'and' between your two letters: ")
   print("༼ つ ╹ 8╹ ༽つ")

   if input_puzzle_4.lower() in ("u and i", "uandi"):
       print()
       print("That is correct...\n")
       amountofpuzzlescompleted += 1
       backpack.append("piece_of_candy")
   else:
       print()
       print("That is incorrect...\n")
       lose_health(25)
       amountofpuzzlescompleted += 1
  
   print("Health =", health)
   print("Amount of Puzzles Completed =", amountofpuzzlescompleted, "/", amountofpuzzles_total)
   print("Backpack =", backpack)

def puzzle_5():
   global health, amountofpuzzlescompleted, amountofpuzzles_total, backpack  # noqa: PLW0602
  
   input_puzzle_4 = input("\nIf there are two ducks in front of a duck, two ducks behind a duck, \nand one duck in the middle, how many ducks are there: ")
   print("  .-─-.  ")
   print(" ( o o ) ")
   print(" |  1  | ")
   print("  V-V-V ")
   if input_puzzle_4.lower() in ("3", "3 ducks"):
       print()
       print("That is correct...\n")
       amountofpuzzlescompleted += 1
       backpack.append("lollypop")
   else:
       print()
       print("That is incorrect...\n")
       lose_health(25)
       amountofpuzzlescompleted += 1
  
   print("Health =", health)
   print("Amount of Puzzles Completed =", amountofpuzzlescompleted, "/", amountofpuzzles_total)
   print("Backpack =", backpack)

def puzzle_6():
   global health, amountofpuzzlescompleted, amountofpuzzles_total, backpack  # noqa: PLW0602
  
   input_puzzle_6 = input("\nEnter a 5 digit code. There were hints in previous puzzles: ")

   if input_puzzle_6 == "27381":
       print()
       print("That is correct...\n")
       amountofpuzzlescompleted += 1
       backpack.append("candy_bar")
   else:
       print()
       print("That is incorrect...\n")
       lose_health(25)
       amountofpuzzlescompleted += 1
  
   print("Health =", health)
   print("Amount of Puzzles Completed =", amountofpuzzlescompleted, "/", amountofpuzzles_total)
   print("Backpack =", backpack)

def puzzle_7():
   global health, amountofpuzzlescompleted, amountofpuzzles_total, backpack  # noqa: PLW0602
  
   print("\na=@ b=x c=U d=J e=| f=ø g=( h=) i=⇩ j=+ k=- l=~\nm=} n={ o=|| p== q=* r=꩜  s=✪ t=✧ u=⌖ v=t w=% \nx=y y=^ z=⊬ \n")
    print("U@{ ^||⌖ |✪U@=|")
   input_puzzle_7 = input("\nTranslate the code written above: ")

   if input_puzzle_7.lower() == "can you escape":
       print()
       print("That is correct...\n")
       amountofpuzzlescompleted += 1
       backpack.append("king_sized_candy_bar")
   else:
       print()
       print("That is incorrect...\n")
       lose_health(25)
       amountofpuzzlescompleted += 1
  
   print("Health =", health)
   print("Amount of Puzzles Completed =", amountofpuzzlescompleted, "/", amountofpuzzles_total)
   print("Backpack =", backpack)



def lose_health(amount):
   global health
   health = max(0, health - amount)



def endings():
   global health, amountofpuzzlescompleted, amountofpuzzles_total, backpack  # noqa: PLW0602
  
   if health == 0:
       print("You were unable to escape.")
       print("      .-''''-.  ")
       print("    (         ) ")
       print("    | (o)  (o) |")
       print("    |          |")
       print("    |     O    |")
       print("    |          |")
       print("    V V V V V V ")
       print("The ghosts caught you!")
      
   elif health < 100 and health > 0:
       print("You barely escaped.")
       print("༼ つ ╹ o╹ ༽つ")
       print("You completed most of the puzzles correctly.")
  
   elif health == 100:
       print("You escaped!")
       print("             ^")
       print("            _[]_")
       print("           (____)")
       print("           | [] |   ^")
       print("      _ _  |____|  ")
       print("    _|_|_|_|____|_ ")
       print("   |  _   _    _  |")
       print("   | [ ] [ ]  [ ] |")
       print("   |  _   _   _   |")
       print("   | [ ] | | [ ]  |")
       print("___|_|_|_|_|_|_|_|___")
       print("But are you really safe?")
      


puzzle_2()
puzzle_4()
puzzle_5()
puzzle_6()
puzzle_7()
endings()
