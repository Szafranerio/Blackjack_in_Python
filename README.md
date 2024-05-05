Source: freecodecamp.org

 ***Card and Deck Management***

**__init__(self, suit, rank)** in the Card class:
Initializes a card with a suit (e.g., Hearts, Diamonds) and a rank (e.g., A for Ace, 10, J for Jack). This method sets up the card's attributes for use in the game.

**__str__(self)** in the Card class:
Returns a string representation of the card, making it easier to display the card information during gameplay.

**__init__(self)** in the Deck class:
Initializes a new deck of 52 cards, covering all suits and ranks. This method populates the deck with a comprehensive set of cards ready for shuffling and dealing.

**shuffle(self)**:
Shuffles the cards within the deck to ensure randomness in card distribution, using Python’s built-in random.shuffle().

**deal(self, number)**:
Deals a specified number of cards from the deck, removing them from the deck and returning them to the caller. This method is crucial for distributing cards to players and the dealer.

***Hand Management***

**__init__(self, dealer=False)** in the Hand class:
Initializes a hand, optionally marking it as the dealer’s hand. This distinction helps in controlling the visibility of the dealer's cards during the game.

**add_card(self, card_list)**:
Adds a list of cards to the hand. This method is used every time a player or dealer hits.

**calculate_value(self)**:
Calculates the total value of the hand based on card values, adjusting for the ace being either 1 or 11 depending on the hand's total value to avoid busting.

**get_value(self)**:
Returns the calculated value of the hand, useful for checking conditions for busting, standing, or hitting.

**is_blackjack(self)**:
Checks if the hand's value is exactly 21, which is a Blackjack.
display(self, show_all_dealer_cards=False):
Prints out the contents of the hand. For the dealer's hand, it can hide the first card (facing down) unless it's time to reveal it at the end of the game play.

***Game Logic***

**play(self)** in the Game class:
Manages the overall game flow, including setting up the deck, dealing initial cards, and managing user input for hits or stands. It also controls the sequence of gameplay events and transitions between different stages of the game.

**check_winner(self, player_hand, dealer_hand, game_over=False)**:
Evaluates the winning conditions of the game, deciding whether the player or dealer wins, or if there is a tie. It handles conditions both during and at the end of the game to determine outcomes based on the rules of Blackjack.
