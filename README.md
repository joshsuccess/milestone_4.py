# milestone_4.py
Hangman Project_Create the Class

import random

class Hangman:
    def __init__(self, word_list, num_lives=5):
        self.word_list = word_list
        self.num_lives = num_lives
        self.list_of_guesses = []
        self.word = self.choose_random_word()
        self.word_guessed = ['_'] * len(self.word)
        self.num_letters = len(set(self.word))

    def choose_random_word(self):
        return random.choice(self.word_list)


# Create an instance of the Hangman class
hangman_game = Hangman(["apple", "banana", "orange", "strawberry", "blueberry"])

# Access attributes of the Hangman instance
print("Word to guess:", hangman_game.word)
print("Word guessed:", hangman_game.word_guessed)
print("Number of unique letters:", hangman_game.num_letters)
print("Number of lives:", hangman_game.num_lives)
print("Word list:", hangman_game.word_list)
print("List of guesses:", hangman_game.list_of_guesses)

Word to guess: strawberry
Word guessed: ['_', '_', '_', '_', '_', '_', '_', '_', '_', '_']
Number of unique letters: 8
Number of lives: 5
Word list: ['apple', 'banana', 'orange', 'strawberry', 'blueberry']
List of guesses: []
