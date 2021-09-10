---
layout: project
type: project
image: images/blackjack-image1.PNG
title: Text-Based Blackjack
permalink: projects/blackjack
# All dates must be YYYY-MM-DD format!
date: 2020-12-02
labels:
  - Java
  - Card Game
  - Programming
summary: A text-based blackjack game made for one of the final projects I've done in ICS 111.
---
<img class="ui medium right floated rounded image" src="../images/blackjack-image.PNG">

Text-based black is one of the final projects I have done for ICS 111. My version of blackjack is meant to be played on the console log of Java Eclipse IDE.
The game features all the major features of the traditional blackjack, such as stand, hit, double-down, split hand, etc.

Other than the help I got from the TA, Jesse McDonald, the entire programming of blackjack was done by myself.

This project made me realize the limit of using only console log to display the game/program. After finishing the project, I was satisfied with the final result, but it also made me think how I could have improved on it through the addition of GUI. Although how well the program for the game is written, the lack of visual elements to show the users what the game is about seemed critical, even to a simple card game like blackjack. Later on, I was able to implement very simple GUIs on my other final project, which is the Inverse Tic-Tac-Toe. 

Here are some of the codes I have used to create text-based blackjack. This code handles the hardest part of the program, where the code determines whether the value of the
Ace is going to be taken as 1 or 11, since the value of the Ace changes based on how many ace cards you have in your hand. For instance, having only 1 ace has a value of 11, but after that, all other aces are considered as 1 only:

```Java
// Calculating the Value of Dealer's card
for (int i = 0; i < dealerHand.size(); i++) {
	Card c = dealerHand.get(i);
		if ((c.getRank() == 1)) {
			dealerAceCount++;
		}

		if ((c.getRank() != 1)) {
			dealerValue += c.getRank();
		}
}
if (dealerAceCount > 0) {
	for (int i = 1; i <= dealerAceCount; i++) {
		if (dealerValue + 11 > 21) {
			dealerValue++;
		} else {
			dealerValue += 11;
		}
	}
}
```





