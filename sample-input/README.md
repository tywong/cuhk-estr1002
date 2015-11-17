# Othello Sample Test Cases

This repo contains the sample input files as well as the expected outcome from the game. Every game should starts with the following game board:

```
    0   1   2   3   4   5   6   7
  +---+---+---+---+---+---+---+---+
0 |   |   |   |   |   |   |   |   |
  +---+---+---+---+---+---+---+---+
1 |   |   |   |   |   |   |   |   |
  +---+---+---+---+---+---+---+---+
2 |   |   |   |   |   |   |   |   |
  +---+---+---+---+---+---+---+---+
3 |   |   |   | @ | O |   |   |   |
  +---+---+---+---+---+---+---+---+
4 |   |   |   | O | @ |   |   |   |
  +---+---+---+---+---+---+---+---+
5 |   |   |   |   |   |   |   |   |
  +---+---+---+---+---+---+---+---+
6 |   |   |   |   |   |   |   |   |
  +---+---+---+---+---+---+---+---+
7 |   |   |   |   |   |   |   |   |
  +---+---+---+---+---+---+---+---+
```

We mandate that:

  - `O` means the white player;
  - '@' means the black player;
  - The `O` player always makes the first move.

## Input file format

The input file contains a series of lines. One each line, a pair of numbers representing the location of the input. 
For example, the following list is the beginning few lines of the first input file.
```
2 3     # player O
2 4     # player @
2 5     # player O
1 4     # player @
```

In case that a player needs to pass the game, it is no indicated in the input file. That is to say, if the i-th input pair results in the situation that Player `O` has to pass his turn, then the i+1-th input pair should still a move platformed by Player `@`.
```
2 3     # player O
2 4     # player @ -> will force player O to pass
2 5     # player @
1 4     # player O
```

## Sample Output

We provide two test cases for you and they should be comprehensive enough for you to test all features in the game.

- The first case, included in the directory `test1`, is a draw-game case, with inputs such that players are occasionally forced to pass his turn.
    
    ```
        0   1   2   3   4   5   6   7
      +---+---+---+---+---+---+---+---+
    0 | @ | O | O | O | O | O | O | O |
      +---+---+---+---+---+---+---+---+
    1 | @ | @ | @ | @ | @ | @ | @ | @ |
      +---+---+---+---+---+---+---+---+
    2 | @ | @ | @ | O | O | O | O | @ |
      +---+---+---+---+---+---+---+---+
    3 | @ | @ | @ | @ | O | @ | O | @ |
      +---+---+---+---+---+---+---+---+
    4 | @ | @ | @ | O | O | O | @ | @ |
      +---+---+---+---+---+---+---+---+
    5 | O | @ | O | @ | O | @ | O | @ |
      +---+---+---+---+---+---+---+---+
    6 | O | O | @ | O | @ | O | O | @ |
      +---+---+---+---+---+---+---+---+
    7 | O | O | O | O | O | O | O | @ |
      +---+---+---+---+---+---+---+---+
    ```


- The second case, included in the directory `test2`, is a fast game with a player's discs all removed.
    
    ```
        0   1   2   3   4   5   6   7
      +---+---+---+---+---+---+---+---+
    0 | O |   |   | O |   | O |   |   |
      +---+---+---+---+---+---+---+---+
    1 |   | O |   | O | O |   | O |   |
      +---+---+---+---+---+---+---+---+
    2 |   | O | O | O |   | O |   |   |
      +---+---+---+---+---+---+---+---+
    3 |   |   | O | O | O |   |   |   |
      +---+---+---+---+---+---+---+---+
    4 |   | O | O | O | O |   |   |   |
      +---+---+---+---+---+---+---+---+
    5 |   |   |   |   |   | O |   |   |
      +---+---+---+---+---+---+---+---+
    6 |   |   |   |   |   |   |   |   |
      +---+---+---+---+---+---+---+---+
    7 |   |   |   |   |   |   |   |   |
      +---+---+---+---+---+---+---+---+
    ```



