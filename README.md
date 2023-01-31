# GUESS-THE-NUMBER




import random
print("\nHello, Welcome to the game. \n What's your name?")
name=input()
print("\nNice to see you",name,". \n In this game you will have to guess the number between 1 and 20.\n Remember you only has 6 chances to complete this game. \n Good luck!")


def guess():
    ran = random.randint(1,20)
    guess=0
    while(guess<6):
        a=input()
        if(a!=ran):
            print("\n\nWrong Guess!, This was your",int(guess) + 1," guess. Try again.")
            if(int(a) < int(ran)):
                print("\n The number you guess is less than the number you have to guess.")
            elif(int(a) > int(ran)):
                print("\n The number you guess is greater than the number you have to guess.")
            elif(int(a) == int(ran)):
                print("\n\n\nCONGRATULATIONS!, YOU WON THE GAME.")
                print("\nWell Played!, You guess the number in", int(guess) + 1,"guess.")
                break
        guess=guess+1
    if(int(guess) == 6):
        print("YOU LOOSE THE GAME.")
    ch=input("Do you want to play again(y/n):")
    if(ch == 'y'):
        guess()

guess()
