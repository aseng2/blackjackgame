# blackjackgame
Blackjack is a casino banking game where the player competes against the house or casino to have the best hand of cards. Unlike many other familiar card games, the players do not compete against each other or help one another. The game is played using one or more decks of common playing cards, also known as a French decks.

In the game, the dealer represents the house/bank/casino. There must be at least one player. The dealer shuffles 8 decks of cards and cuts the deck. A _cut card_ is placed randomly between the 60th and 80th card from the bottom of the deck. All the cards are placed in a [_shoe_](https://en.wikipedia.org/wiki/Shoe_(cards)) which the dealer uses to deal cards one at a time. When the dealer reaches the _cut card_, then, when the game ends, the cards are shuffled, cut, a _cut card_ is placed, and the cards are returned to the _shoe_.

The dealer deals cards to the players from their left to their right. Each player receiving one card face up. The dealer deals themself a face up card and then deals another card to each player. Finally, the dealer deals one face down card to themself.

Once the cards are dealt, each player has a turn. Starting with the first player, the player must first decide if she would like to _double down_. 

Once those initial decisions are made, the player chooses to _hit_, take a card, or _stand_, end their turn. The player attempts to reach a sum as close as possible to 21. The sum is calculated by converting the _rank_ of a card to a numerical value. Number cards (2, 3, 4, 5, 6, 7, 8, 9) have a value equal to their rank. Court cards (Jack, Queen, King) have a value equal to 10. Aces can have a value of 1 or 11; whichever is most advantageous to the player. A special case is _blackjack_ or _a natural_ where a player or dealer has an Ace and a card that has a value of 10 such as a 10, Jack, Queen, or King. The suit of a card (Clubs, Hearts, Spades, Diamonds) does not matter in this game.

A player wins when their hand has a higher value than the dealer's yet is not greater than 21. Players that pass 21 are _busted_ which means they loose their bet regardless of what the dealer does.

When a player and the dealer have the same value for their respective hands, then this is a _push_. A _push_ means that no one wins and the player does not lose her wager.

The dealer is always last to play. The dealer begins by turning over the face down card and deciding to _hit_ or _stand_. Unlike the players, the dealer must _hit_ if their hand value is less than 17. If the value of their hand is 17 or greater, then the dealer _stands_. If all the players have already _busted_ the dealer _stands_ thus removing the chance that the dealer may _bust_ as well.

(There are not _splits_.) If the dealer's face up card has a value of 10 or higher, then the player may also buy _insurance_ as a side bet. Some versions of Blackjack allow a player to _surrender_, however our version will not have this rule.

The side bet that is available to a player is _doubling down_. This game does not allow _splits_, buying _insurance_, or _surrendering_.

The player may choose to _double down_ at the start of their turn. To _double down_, the player doubles her bet on her cards and takes one additional card before ending her turn. For example, if the player has an 4 of Diamonds and a King of Hearts, then she may double down believing that she only wants one additional card and that will be enough to beat the dealer. If she is dealt a 7, she has 21. Otherwise, any card less than an 8 will keep her in the game. Should the dealer lose then the player earns winnings on her initial wager and on her _double down_ bet. The _double down_ bet must be equal to the player's initial wager. A player must have the funds in her bank roll to _double down_.

All bets are _two-to-one_ payout. In other words, if a player wagers $5 and wins, then the casino pays the player $5 and the player keeps the original wager thus pocketing a total of $10.

In our game, the dealer shall be played by a game AI. Although not required, you may find it advantageous to have bots play as well to test the game and to make the game more interesting for single players. All players start with $10,000.00 in their bank balance. The minimum bet is $1 and the maximum bet is the player's bank balance. When a player goes broke (loses all of her money), then the player is offered $10,000.00 from an anonymous donor.

Most importantly, the player shall be able to exit the game and restart the game and have the same bank balance when the game is restarted. This means that players must use a unique identifier to start the game which can be a name, handle, email address, etc. The identifier is used to track the player's progress such that their bank balance from previous games can be reused.


If there is more than one player, the game is played as a [hotseat](https://en.wikipedia.org/wiki/Hotseat_(multiplayer_mode)) multiplayer game.

## Rules

* There is at least one players playing the game and at most four.
* To start the game, a player can enter the number 1 through 4 to establish how many players there are.
* All players start with $10,000.00 in their bank balance.
* The dealer is always a computer AI and has unlimited funds.
* The game is turn based.
* All players have a name, including the _computer AI_. Players' names may be used as unique identifiers or additional information can be gathered.
* Unique identifiers are used to serialize the game state to a file so that a player can have their bank balance upon return to the game.
* The game is played with 8 decks of cards. The cards are typical cards with the ranks Ace, 2, 3, 4, 5, 6, 7, 8, 9, 10, Jack, Queen, King and the suits Clubs, Hearts, Spades, Diamonds. There are no jokers.
* The value of the cards is the rank of the card except for Ace, Jack, Queen, and King. An Ace's value is either 1 or 11 depending on what is most advantageous to the hand in question. Jacks, Queens, and Kings have a value of 10.
* Before playing, the cards must be shuffled and cut.
* A cut card is placed randomly between the 60th and 80th card from the bottom of the deck.
* The players play in the order their names are entered when the program starts. The dealer always goes last.
* Once each player has had a turn in ascending order, the turn returns to the first player. (The process is a circular queue.)
* The game is made up of many games. The players continue playing games of blackjack. At the end of every game, the game prompts the first player if they would like to play again. An answer of _yes_ means the dealer will deal cards out to the same players who played previously. With multiple players, should one choose to leave then the first player must answer _no_ to end the game and exit the program.
* At the start of every game, before cards are dealt, each player must place a wager. A wager can be at least $1 and at most their bank balance.
* A player may not wager more money than she has in her bank balance.
* The cards are dealt one by one, starting with the first player and ending on the dealer.
* The dealer's second card is kept hidden from the players; all other cards are dealt face up.
* At the beginning of every turn, the game displays what cards the current player is holding and what face up card the dealer has showing.
* Whenever a card is dealt, it is printed or shown to the players before taking any other action.
* When it is the dealer's turn, the dealer must turn over (print or show) the face down card before taking any other action.
* All bets pay out 2 to 1.
* When a players turn begins, they have the option to _double down_.
* A player may not _surrender_, _split_, or buy _insurance_.
* The player may _double down_ when her turn starts and never later.
* The player may _double down_ if and only if there is sufficient funds in her balance to double her wager.
* A player is prompted to _hit_ or _stand_ unless they are _busted_ or have _21_. If they have _busted_ or have _21_ then a message is shown stating that they have _busted_ or reached _21_.
* The dealer must _hit_ on a hand that is less than 17. The dealer must _stand_ on a hand that is 17 or greater.
* The dealer only _hits_ if there are players who are not _busted_.
* No one wins or loses when there is a _push_.
* A dealer does not place bets which means the dealer does not _double down_.


To summarize the order of game play operations:
1. If needed, cards are shuffled, cut, and a cut card is placed in a position between the 60th and 80th card from the bottom.
1. For each player, a wager is entered before the cards are dealt.
1. Cards are dealt one at a time starting with the first player, continuing through to the last player, and ending on the dealer. This is done twice such that each player and the dealer has two cards. The dealer's last card is kept face down until it is the dealer's turn.
1. For each player, begin their turn.
    1. For each hand, offer to _double down_. For each _double down_ wager, the player's wager is doubled.
    1. While the player's hand is less than 21 or is not busted, offer the player to _hit_ or _stand_. When the player _hits_ deal an additional card. If the player _stands_, then the player's turn concludes.
1. The dealer plays last. If there exists a player who is not busted, then the dealer must play their hand according to the rules. Otherwise, the dealer stands.
1. For each player, determine if the player has won, lost, or _pushed_. Update all the players' balances to reflect the outcome of the game.
