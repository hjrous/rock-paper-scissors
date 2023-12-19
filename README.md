import random

def play_rock_paper_scissors():
    print("Welcome to Rock, Paper, Scissors!")
    
    choices = ["rock", "paper", "scissors"]
    computer_choice = random.choice(choices)

    while True:
        player_choice = input("Enter your choice (rock, paper, or scissors): ").lower()

        if player_choice not in choices:
            print("Invalid choice. Please choose rock, paper, or scissors.")
            continue

        print(f"Computer chose: {computer_choice}")
        print(f"You chose: {player_choice}")

        if player_choice == computer_choice:
            print("It's a tie!")
        elif (
            (player_choice == "rock" and computer_choice == "scissors") or
            (player_choice == "paper" and computer_choice == "rock") or
            (player_choice == "scissors" and computer_choice == "paper")
        ):
            print("You win!")
        else:
            print("You lose!")

        play_again = input("Do you want to play again? (yes/no): ").lower()
        if play_again != "yes":
            print("Thanks for playing. Goodbye!")
            break

if __name__ == "__main__":
    play_rock_paper_scissors()
