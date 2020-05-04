# Project 2: Blackjack Rubric

## Part 1: Player

### Q1: Player constructor

Complete the constructor by following the documentation and the tests.

- +10: All fields set correctly. (Passes autograder)

### Q2: Place wager

Request that the player place a wager. *Be sure to read the note about using `input_func`.*
- +20: Passes autograder.
- -5: Doesn't loop while the player has not placed a valid wager.
- -3: Doesn't check if the wager is valid.
- -2: Doesn't use `input_func` in place of `input`.
- -2: Doesn't cast wager to `int`.
- -5: Doesn't request the player to make a wager.
- -3: Doesn't set the `self.wager` attribute.

### Q3: Win chips

The player wins its wager.
- +10: Passes autograder.

### Q4: Lose chips

The player loses its wager.
- +10: Passes autograder.

### Q5: Receive card

The player receives a card. When the player receives an ace, it will start with value 11. If the player's total goes above 21, an ace should be reduced in value to 1, if there are any. Use the attributes `self.num_aces` and `self.reduced_aces` to keep track of how many aces there are, and how many aces have been reduced in value respectively.
- +30: Passes autograder.
- -5: Adds a string representation of the card instead of the card.
- -5: Doesn't check for ace correctly.
- -5: Doesn't check for face card correctly.
- -5: Doesn't reduce the value of an ace if the resulting total is above 21.
- -3: Doesn't check to see if there is a remaining ace that has not been reduced before reducing it.
- -5: Doesn't update attributes correctly.
- -2: Missing print statements.

### Q6: Do turn

Does the player's turn.
- +20: Passes autograder.
- -5: Doesn't loop correctly.
- -5: Doesn't process user input correctly.
- -5: Doesn't give card to player correctly.
- -5: Incorrect condition for when the player's turn is over.

### Q7: Do dealer turn

Does the dealer's turn. A dealer will continue to hit until his card total is below 18.
- +15: Passes autograder.
- -5: Loops incorrectly.
- -5: Dealer receives card incorrectly.

## Part 2: Game

### Q8: Game constructor

Complete the game constructor.
- +10: Correct.

### Q9: Deal cards

Deals 2 cards to each player, and to the dealer. Each player should be dealt 2 cards before the dealer to make sure the output matches the tests. `player.receive_card()` must be complete for the tests for this question to pass.
- +20: Passes autograder.
- -5: Doesn't loop through players.
- -5: Doesn't loop twice to deal two cards to each player.
- -5: Doesn't deal cards to dealer.

### Q10: Finish round

Finish a round and dole out winnings and losses. To be clear, a dealer that goes bust has a card total of 0. However, a player who has gone bust does not beat a dealer who has gone bust. A tie goes in favor of the dealer.
- +15: Passes autograder.
- -5: Doesn't loop through all players.
- -5: Doesn't check win and loss conditions correctly.
- -5: Doesn't award/take chips from players correctly.

### Q11: Check chip totals

Check to see if any players have gone broke.
- +15: Passes autograder.
- -5: Doesn't loop through players.
- -5: Doesn't check if player has gone broke correctly.
- -5: Doesn't remove all players from list correctly. (Either two passes, or removes from back of list.)

### Q12: Play game

Tie everything together.
- +20: Correct.
- -5: Doesn't loop while there are players left.
- -5: Doesn't ask players to place wagers.
- -5: Doesn't ask players to do turn.
- -3: Doesn't make dealer do turn.
- -2: Doesn't call `finish_round()`, `check_chip_totals()` and `reset()` at the end.
