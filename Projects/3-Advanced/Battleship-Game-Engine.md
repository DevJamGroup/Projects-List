# Battleship Game Engine

**Tier:** 3-Advanced

Battleship is a strategy type guessing game for two players. It is played on ruled grids (paper or board) on which each player's fleet of warships are marked. The locations of the fleets are concealed from the other player. Players alternate turns calling "shots" at the other player's ships, and the objective of the game is to destroy the opposing player's fleet. 

Before play begins, each player secretly arranges their ships on their primary grid. Each ship occupies a number of consecutive squares on the grid, arranged either horizontally or vertically. The number of squares for each ship is determined by the type of ship. The ships cannot overlap (i.e., only one ship can occupy any given square in the grid). The types and numbers of ships allowed are the same for each player. These may vary depending on the rules. The ships should be hidden from players sight and it's not allowed to see each other's pieces. The game is a discovery game which players need to discover their opponents ship positions. [11]

This challenge is for you to create a Battleship game that allows the user to play against a computer.

## User Stories

### BGE

-   [ ] User can invoke a `startGame()` function to begin a 1-player game. This function will generate an 8x8 game board consisting of 3 ships having a width of one square and a length of:

    -   Destroyer: 2 squares
    -   Cruiser: 3 squares
    -   Battleship: 4 squares

    `startGame()` will randomly place these ships on the board in any direction and will return an array representing ship placement.

-   [ ] User can invoke a `shoot()` function passing the target row and column coordinates of the targeted cell on the game board. `shoot()` will return indicators representing if the shot resulted in a hit or miss, the number of ships left (i.e. not yet sunk), the ship placement array, and an updated hits and misses array.

    Cells in the hits and misses array will contain a space if they have yet to be targeted, `O` if they were targeted but no part of a ship was at that location, or `X` if the cell was occupied by part of a ship.

### Text-based Presentation Layer

-   [ ] User can see the hits and misses array displayed as a 2 dimensional character representation of the game board returned by the `startGame()` function.
-   [ ] User can be prompted to enter the coordinates of a target square on the game board.
-   [ ] User can see an updated hits and misses array display after taking a shot.
-   [ ] User can see a message after each shot indicating whether the shot resulted in a hit or miss.
-   [ ] User can see an congratulations message after the shot that sinks the last remaining ship.
-   [ ] User can be prompted to play again at the end of each game. Declining to play again stops the game.

## Bonus features

### BGE

-   [ ] Additional ships: Carrier: 5 squares, Submarine: 3 squares.
-   [ ] User can manually place their objects(ships) in desired location.
-   [ ] User can specify the number of rows and columns in the game board as a parameter to the `startGame()` function.
-   [ ] User can invoke a `gameStats()` function that returns a Javascript object containing metrics for the current game. For example, number of turns played, current number of hits and misses, etc.
-   [ ] User can specify the number of players (1 or 2) when calling `startGame()` which will generate one board for each player randomly populated with ships.

    `shoot()` will accept the player number the shot is being made for along with the coordinates of the shot. The data it returns will be for that player.

### Text-based Presentation Layer

-   [ ] User can see the current game statics at any point by entering the phrase `stats` in place of target coordinates. (Note that this requires the `gameStats()` function in the BGE)
-   [ ] User can specify a two player game is to be played, with each player alternating turns in the same terminal session (Note that this requires corresponding Bonus Features in the BGE)
-   [ ] User can see the player number in prompts associated with the inputs in each turn.
-   [ ] User can see both players boards at the end of each turn.

## Useful links and resources

-   [Battleship Game (Wikipedia)](<https://en.wikipedia.org/wiki/Battleship_(game)>)
-   [Battleship Game Rules (Hasbro)](https://www.hasbro.com/common/instruct/battleship.pdf)

## Example projects

This YouTube video shows how a text-based [Battleship Game](https://www.youtube.com/watch?v=TKksu3JXTTM) is played.

The following example is provided as a demonstration of the Battleship game if it is unfamiliar to you. Remember you are to implement a text based presentation layer for testing.

-   [Battleship Game by Chris Brody](https://codepen.io/CodifyAcademy/pen/ByBEOz)
