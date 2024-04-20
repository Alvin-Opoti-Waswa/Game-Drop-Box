import random

class GuessingGame:
    def __init__(self, name, max_attempts=3):
        self.name = name
        self.max_attempts = max_attempts
        self.secret_number = random.randint(1, 10)
        self.attempts = 0
        self.correct_guess = False

    def play_game(self):
        print(f"Welcome, {self.name}! I have selected a number between 1 and 10. Can you guess it?")

        while self.attempts < self.max_attempts:
            guess = int(input("Enter your guess: "))
            self.attempts += 1

            if guess == self.secret_number:
                print(f"Congratulations, {self.name}! You guessed the correct number.")
                self.correct_guess = True
                break
            else:
                print("Incorrect guess. Try again.")
                remaining_attempts = self.max_attempts - self.attempts
                print(f"You have {remaining_attempts} {'attempts' if remaining_attempts > 1 else 'attempt'} remaining.")

        if not self.correct_guess:
            print(f"Sorry, {self.name}, you've run out of attempts. The correct number was {self.secret_number}.")

    def display_player_info(self):
        print("\nPlayer Information:")
        print(f"Name: {self.name}")
        print(f"Attempts: {self.attempts}")
        print("Game Status: " + ("Win" if self.correct_guess else "Loss"))



player_name = input("Enter your name: ")
game_instance = GuessingGame(name=player_name)
game_instance.play_game()
game_instance.display_player_info()
