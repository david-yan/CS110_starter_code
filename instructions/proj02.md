# Project 2: Blackjack

## Background
In this project, you will be finishing the implementation of Blackjack using the OOP design we came up with in class. This will be a simplified version of the game, and not include all of the rules played in casinos. Be sure to read to rules so you know which are included, and which are not. Additionally, the `Card` and `Decks` classes have been provided with an implementation. You can feel free to use your own `Card` and `Decks` classes from homework, so long as the function the same way. 

## Summary of game rules
To review, these are the rules of blackjack that we will be implementing:
- At the beginning of the game, all players are given a number of chips.
- At the beginning of each round, each player places a wager and bets a certain amount of their chips.
- Each player in the game is playing against the "dealer". 
  - If the player beats the dealer, that player wins the amount of chips that they wagered.
  - If the player loses to the dealer, that player loses the amount of chips that they wagered.
- After all players have placed a wager, all players (including the dealer) is dealt two cards.
- For each player (dealer goes last), they take their turn. The goal of the player during their turn is to get their card
total to be as close to, but not over 21. To do this, each player is given two options for their turn:
  - Hit: The player receives a new card. The player can continuously choose to "hit" as many times as they want until their
  card total goes above 21, in which case they go "bust".
  - Stand: The player ends their turn with their current card total.
- After all players have gone, the players who have a higher card total than the dealer and have not gone "bust" beat the
dealer. All other players lose to the dealer.

The value of cards are as follows:
- Suits don't translate into any value.
- Ace has either a value of 1 or 11. From the way we will implement this program, an ace will always be added with a value of 11, and can be reduced to 1 to prevent the player from going bust.
- Cards 2-10 translate exactly to their card value.
- All face cards (J, Q, K) have a value of 10.

## Starter Files
Download [proj02.zip](https://github.com/david-yan/CS110_starter_code/blob/master/proj02.zip?raw=true). Inside the archive,
you will find the following files:
- `player.py` - The file that contains the Player class. Part 1 of the project.
- `game.py` - The file that contains the Game class. Part 2 of the project.
- `card.py` - The file that contains the Card and Decks classes, implementations provided.
- `blackjack.py` - The file that will run the program. *DO NOT MODIFY THIS FILE.*
- `ok` - Autograder program. *DO NOT MODIFY THIS FILE.*
- `proj02.ok` - Configuration for the autograder. *DO NOT MODIFY THIS FILE.*
- `tests/` - A directory that contains all of the tests. *DO NOT MODIFY THIS FILE.*

## Running Tests
To test that your code is working correctly, run `python3 ok`. This will automatically run the test suite against your code.
Please make sure to check your output to ensure that all of the tests passed. If you have any problems running the tester,
please make a post on Piazza.

#### The following questions are meant to be completed in order.

## Part 1: Player

This file should be completed from the top downwards. To make sure that these instructions are not too verbose, the code has not been copied here. Instead, only clarifying details will be put here. Please make sure to check these instructions before completing the functions.

### Q1: Player constructor

Complete the constructor by following the documentation and the tests.

```
python3 ok -q player
```

### Q2: Place wager

Request that the player place a wager. *Be sure to read the note about using `input_func`.*

```
python3 ok -q place_wager
```

### Q3: Win chips

The player wins its wager.

```
python3 ok -q win_chips
```

### Q4: Lose chips

The player loses its wager.

```
python3 ok -q lose_chips
```

### Q5: Receive card

The player receives a card. When the player receives an ace, it will start with value 11. If the player's total goes above 21, an ace should be reduced in value to 1, if there are any. Use the attributes `self.num_aces` and `self.reduced_aces` to keep track of how many aces there are, and how many aces have been reduced in value respectively.

```
python3 ok -q receive_card
```

### Q6: Do turn

Does the player's turn.

```
python3 ok -q do_turn
```

### Q7: Do dealer turn

Does the dealer's turn. A dealer will continue to hit until his card total is below 18.

```
python3 ok -q do_dealer_turn
```

## Part 2: Game

This file should also be completed from the top downwards.

### Q8: Game constructor

Complete the game constructor.

```
python3 ok -q game
```

### Q9: Deal cards

Deals 2 cards to each player, and to the dealer. Each player should be dealt 2 cards before the dealer to make sure the output matches the tests. `player.receive_card()` must be complete for the tests for this question to pass.

```
python3 ok -q deal_cards
```

### Q10: Finish round

Finish a round and dole out winnings and losses. To be clear, a dealer that goes bust has a card total of 0. However, a player who has gone bust does not beat a dealer who has gone bust. A tie goes in favor of the dealer.

```
python3 ok -q finish_round
```

### Q11: Check chip totals

Check to see if any players have gone broke.

```
python3 ok -q check_chip_counts
```

### Q12: Play game

Tie everything together.

No autograder tests for this part. Once this is complete, run the following to play blackjack:
```
python3 blackjack.py
```

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/proj02/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

### Be sure to submit your entire proj02 directory.
