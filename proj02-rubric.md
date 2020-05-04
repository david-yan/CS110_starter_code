# Project 2: Blackjack Rubric

## Part 1: Player

This file should be completed from the top downwards. To make sure that these instructions are not too verbose, the code has not been copied here. Instead, only clarifying details will be put here. Please make sure to check these instructions before completing the functions.

### Q1: Player constructor

Complete the constructor by following the documentation and the tests.

### Q2: Place wager

Request that the player place a wager. *Be sure to read the note about using `input_func`.*

### Q3: Win chips

The player wins its wager.

### Q4: Lose chips

The player loses its wager.

### Q5: Receive card

The player receives a card. When the player receives an ace, it will start with value 11. If the player's total goes above 21, an ace should be reduced in value to 1, if there are any. Use the attributes `self.num_aces` and `self.reduced_aces` to keep track of how many aces there are, and how many aces have been reduced in value respectively.

### Q6: Do turn

Does the player's turn.

### Q7: Do dealer turn

Does the dealer's turn. A dealer will continue to hit until his card total is below 18.

## Part 2: Game

### Q8: Game constructor

Complete the game constructor.

### Q9: Deal cards

Deals 2 cards to each player, and to the dealer. Each player should be dealt 2 cards before the dealer to make sure the output matches the tests. `player.receive_card()` must be complete for the tests for this question to pass.

### Q10: Finish round

Finish a round and dole out winnings and losses. To be clear, a dealer that goes bust has a card total of 0. However, a player who has gone bust does not beat a dealer who has gone bust. A tie goes in favor of the dealer.

### Q11: Check chip totals

Check to see if any players have gone broke.

### Q12: Play game

Tie everything together.
