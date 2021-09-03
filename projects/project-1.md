---
layout: project
type: project
image: images/ittt-image.PNG
title: Inverse Tic-Tac-Tpe
permalink: projects/ITTT
# All dates must be YYYY-MM-DD format!
date: 2020-12-03
labels:
  - Video Game
  - Programming
  - Java
summary: For the final project for ICS 111, I created a variant of Tic-Tac-Toe, the Inverse Tic-Tac-Toe.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/ittt-image.PNG">
</div>

Inverse Tic-Tac-Toe (ITTT) is a variant of the game Tic-Tac-Toe we know of. Unlike the traditional Tic-Tac-Toe, which is a two player game where the player that can create 3 in
a row first before the opponent wins the game, the ITTT is the complete opposite, where you have to force the opponent to get 3 shapes in a row to win the game. It's also a one player game with AI as the opponent. The project was solely programmed on Java Eclipse IDE with GUI being implemented.

Here is some example of the code I used for ITTT:
```Java 
// Drawing the player's Symbol
			for (int i = 0; i < 3; i++) {
				for (int j = 0; j < 3; j++) {
					if (player[i][j] == true) {
						grp.setColor(Color.red);
						grp.drawLine(200 * j + 50, 200 * i + 50, 200 * j + 150, 200 * i + 50);
						grp.drawLine(200 * j + 150, 200 * i + 50, 200 * j + 150, 200 * i + 150);
						grp.drawLine(200 * j + 150, 200 * i + 150, 200 * j + 50, 200 * i + 150);
						grp.drawLine(200 * j + 50, 200 * i + 150, 200 * j + 50, 200 * i + 50);
					}
				}
			}
```







