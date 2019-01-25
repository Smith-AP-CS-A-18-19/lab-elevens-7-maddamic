# Elevens 7

Follow the instructions provided for Activity 7 in the student lab guide. This is more of an exploratory lab, so you will not need to copy any of your previous code into the repo. Answer the questions from the Student Guide in this document and ensure that you save and push the repo. You have one week to complete this lab.

1. What items would be necessary if you were playing a game of Elevens at your desk (not on the computer)? List the private instance variables needed for the `ElevensBoard` class.

    You would need a regular deck of cards that had both numbers, face cards, and suits.
    private bOARD_sIZE;
    private rANKS;
    private sUITS;
    private pOINT_vALUES;
    private Deck;

2. Write an algorithm that describes the actions necessary to play the Elevens game.

    Use nine cads, if two cards add up to eleven, they can be removed, replace the two removed cards with two remaining cards from the deck. If a jack, queen, and king are selected they can also be removed. If there are no number cards that add up to 11 and not a jack queen and king then the game will say you lost.

3. Now examine the partially implemented `ElevensBoard.java` file found in this repository. Does the `ElevensBoard` class contain all the state and behavior necessary to play the game?

    It has all the necessary methods to complete the game.

4. `ElevensBoard.java` contains three helper methods. These helper methods are private because they are only called from the ElevensBoard class.

  * a. Where is the `dealMyCards` method called in ElevensBoard?

      It is called in the newGame method and in ElevensBoard.

  * b. Which `public` methods should call the `containsPairSum11` and `containsJQK` methods?

      The isLegal method, anotherPlayIsPossible, and replaceSelectedCards.

  * c. It’s important to understand how the `cardIndexes` method works, and how the list that it returns is used. Suppose that `cards` contains the elements shown below. Trace the execution of the `cardIndexes` method to determine what list will be returned. Complete the diagram below by filling in the elements of the returned list, and by showing how those values index `cards`. Note that the returned list may have less than 9 elements.

    * `cards`

| 0  | 1  |  2   | 3  |  4   |  5   | 6  | 7  |  8   |
|:--:|:--:|:----:|:--:|:----:|:----:|:--:|:--:|:----:|
| J♥ | 6♣ |`null`| 2♠ |`null`|`null`| A♠ | 4♥ |`null`|

   *  * Answer(vv)  - This list should contain the indices of the cards, not the cards themselves

| 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| J♥ | 6♣ | 2♠ | A♠ | 4♥ |    |    |    |    |

  * d. Complete the following `printCards` method to print all of the elements of cards that are indexed by `cIndexes`.
```java
  public static printCards(ElevensBoard board) {
      List<Integer> cIndexes = board.cardIndexes();
      for (int i = 0; i < cIndexes.size(); i++) {
        System.out.println(cIndexes.get(i));
      }
  }
```

  * e. Which one of the methods that you identified in question 4b above needs to call the `cardIndexes` method before calling the `containsPairSum11` and `containsJQK` methods? Why?

        The replaceSelectedCards method.

## Feedback
4.c is slightly off
19/20
