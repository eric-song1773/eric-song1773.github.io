---
layout: project
type: project
image: images/cotton-square.png
title: Text-Based Blackjack
permalink: projects/blackjack
# All dates must be YYYY-MM-DD format!
date: 2020-12-02
labels:
  - Java
  - Card Game
summary: A text-based blackjack game made for one of the final projects I've done in ICS 111.
---
<img class="ui image" src="{{ site.baseurl }}/images/cotton-header.png">

Text-based black is one of the final projects I have done for ICS 111. My version of blackjack is meant to be played on the console log of Java Eclipse IDE.
The game features all the major features of the traditional blackjack, such as stand, hit, double-down, split hand, etc.


Here are some of the codes I have used to create text-based blackjack. 

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
						}

						else {
							dealerValue += 11;
						}
					}
				}
```





