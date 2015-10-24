# What are Time Delays? #

Usually called **time control**, chess tournaments and games oftentimes implement some type of special timing scheme during play. One of the most common types of time control is called **compensation**. The basic premise of compensation is that each player will gain some amount of time at the beginning of each of his turns. However, the way in which the extra time is handled varies between different types of time control. Simple Chess Clock currently implements the following types of time control:

## Fischer Delay ##

The **Fischer Delay** scheme is named for its inventor (and chess Grandmaster) Bobby Fischer. When a player's turn begins, the delay time is added to his remaining time, then his clock begins to tick. For example, if a player had 65 seconds remaining and the delay was set to 5 seconds, the beginning of his next turn would put him at 70 seconds.

Since time is added directly to a player's remaining time, it is possible to actually accumulate additional time by making moves quickly. Using the same example from above, if the player makes his move in 2 seconds, then he would retain the extra 3, thus ending his turn with 68 seconds (3 seconds more than he started with).

## Bronstein Delay ##

**Bronstein Delay** is named for its inventor, Soviet grandmaster David Bronstein. At the beginning of a player's turn, his clock will first tick down through some set amount of delay time, effectively waiting the length of the delay. Once the delay time is exhausted, the player's remaining clock time will begin to tick like normal.

Time is not directly added to a player's remaining clock time in Bronstein Delay. Using the same times as above, but a Bronstein system, if the player moves in 2 seconds, he does not gain the extra 3 (it is simply lost). Thus, he can never accumulate time by moving quickly, but he can avoid _losing_ time.