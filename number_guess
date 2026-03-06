import random

def number_guess():
    while True:
        number=random.randint(1,100)
        attempts=0

        print("NUMBER GUESSING GAME")
        print("I'm thinking of a number in between 1 to 100, I dare you to guess it")

        while True:
            try:
                # allow the player to type 'exit' at any prompt to quit immediately
                difficulty_input = input("Choose your difficulty level, 1 to 5 (or type 'exit' to quit): ")
                if difficulty_input.strip().lower() == 'exit':
                    print("Exiting game.")
                    return
                difficulty = int(difficulty_input)
                print()
                if 1 <= difficulty <=5:
                    break
                else:
                    print("Please enter a number between 1 and 5")
            except ValueError:
                    print("Please enter a valid number")
                    
        max_attempts=int(50/difficulty)

        print("NUMBER GUESSING GAME")
        print("I'm thinking of a number in between 1 to 100, I dare you to guess it")

        while attempts<max_attempts:
            try:
                guess_input = input(f"Attempt{attempts+1}: Enter your guess (or 'exit' to quit): ")
                if guess_input.strip().lower() == 'exit':
                    print("Exiting game.")
                    return
                guess = int(guess_input)
            except ValueError:
                print("Please try again")
                continue
        
            attempts +=1

            if guess==number:
                print(f"Correct, You are absolutely, perfectly read me in just {attempts} attempts")
                break
            elif guess<number:
                print("You guessed too low, Try again")
            else :
                print("You guessed too high, Try agian")
        else:
            print(f"Sorry, you have ran out of attempts. The correct number was {number}")
            
        play_again=input("Would you like to play again? (yes/no): ").strip().lower()
        
        if play_again!="yes":
            print("Thanks for playing! Goodbye. ")
            break
        
number_guess()
