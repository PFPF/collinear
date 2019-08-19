# Collinear-Equidistant Gomoku (5 in an AP) | 五子等距共线棋

Welcome to a new variety of Gomoku! Here are the rules and some thoughts.

## Basic rule

If you have played Gomoku (5-in-a-Row), the rule is easy to get: 
> **Instead of having 5 *adjacent* pieces in a row, now you can win with any 5 pieces that are collinear and equidistant.**


This will include all Gomoku's winning configurations, but add a lot more, like this:
![](https://collinear.fei.land/rules/ri.PNG)

In other words, you win if 5 of your pieces form an arithmetic progression (AP) in the 2D metric.

(If you never played 5-in-a-Row, think of tic-tac-toe as 3-in-a-Row.)

#### Exercise
Prove that when there are only 2 players, the first one can win easily.

... which is why it's reasonable to have at least 3 players. In fact, that's how it's initially played after introduced by one of my classmates (very likely Shengyu Zhao).

## Joining the game

Click "Join" to join.

## Game play

In your turn, click an empty spot on the board to put down a piece.

## Force-end a turn

Once in a while, there's someone who disconnects or hibernates during the game, producing an un~~der~~standably (or infinitely) long turn. 

To deal with this, most games use a clock to time the turns and ends the turn when the time is up. But this game is usually played between friends who just want to relax and have fun. We don't want to rush them.

To account for both patience and fairness, we use the following rule:

> **Turns are never interrupted by the system, but if a turn exceeds 60s, every player has an option to force-end the turn, including the current player (who would be altruistic to do that).**

The rigor is in your hands.

## Clear-out

10 minutes after the last move or immediately after a winner is annouced, everyone visiting the page could clear the board.

### Identity security ~~(Hackers manual)~~
When you visit the page, a "password" is dynamically generated and stored in the session storage associated with the current browser tab. It will be preserved upon reloading the page. Almost all game actions will be sent to the server with this password. It proves your identity and prevents others from pretending as you. (Otherwise, imagine you're green and in your turn, someone enters "play green 3 4" or equivalent at the console...)

The hashed password is stored somewhere public, but the hashing function makes it computationally hard to retrieve the password. *The session storage will be cleared when the tab is closed.*

### Todo

 - Visualize current player 
 - Complete bilingual support

Wish you a 5 in an AP!
