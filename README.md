# Rock-paper-Scissors-game
from http.cookiejar import user_domain_match
import random
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
game_image = [rock,paper,scissors]
user_choice = int(input("what would u choose? type 0 for rock,1 for paper and 2 for scissors!\n"))
if user_choice >=0 and user_choice <=2:
    print(game_image[user_choice])



computer_choice= random.randint(0,2)
print("computer chose: ")
print(game_image[computer_choice])

if user_choice >= 3 or user_choice < 0:
    print("you have typed an invalid number.you lost!")
elif user_choice == 0 and computer_choice == 2:
    print("you won!")
elif computer_choice == 0 and user_choice == 2:
    print("you lost!")
elif user_choice == computer_choice:
    print("its a draw!")
elif computer_choice > user_choice:
    print("you lost!")
elif user_choice > computer_choice:
    print("you won!")
