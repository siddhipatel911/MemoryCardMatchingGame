# Memory Card Matching Game 🧠🎴

## Overview
Memory Card Matching Game is a **Java Swing GUI** project where the player flips over pairs of cards to find all matching images before time runs out.  
The cards are shuffled randomly every game, and the player’s score is based on how quickly they match all pairs.

This project showcases Java Swing event-driven programming, randomization, timers, and multi-panel GUI design.

- **Language:** Java  
- **IDE:** NetBeans  
- **GUI Library:** Java Swing  
- **Status:** Complete  

---

## Features

### 🃏 Card Flipping Mechanics
- 12 or more cards arranged in a grid layout.
- Each card hides an image underneath its back design.
- Clicking flips the card to reveal the hidden image.
- Two cards stay flipped if they match; otherwise, they flip back automatically.

### 🔄 Random Layout
- Card positions are randomized each round using Java’s random shuffle.
- Ensures each playthrough is unique and unpredictable.

### ⏱ Timer & Scoring
- A countdown timer starts when the game begins.
- Faster completion times mean higher scores.
- Timer updates are displayed on screen in real time.

### 🧠 Match Logic
- The game checks for matches after every two flips.
- Matches remain visible, mismatched pairs are flipped back after a short delay.
- Tracks total pairs matched.

### 🏆 Game End Conditions
- Win: all pairs matched before the timer ends.
- Lose: timer reaches zero before finishing.
- On game end:
  - A result message pops up (You Win! / Time’s Up!).
  - Option to replay without restarting the program.

### 🖼 GUI Layout
- Grid of card buttons with custom icons (`cardback.jpg`, `image1.jpg`, `image2.jpg`, etc.).
- Start and Reset buttons.
- Live score/timer display at the top of the window.
- Background and button color coordination for a polished interface.

---

## How It Works (Technical)
- **Main frame:** `MatchingGame.java`
  - Initializes the JFrame and loads card images.
  - Sets up grid layout for the cards.
- **Event handling:**
  - Each card button listens for clicks using `ActionListener`.
  - Game logic keeps track of which two cards are currently flipped.
- **Timer:**
  - Uses `javax.swing.Timer` for both the countdown and card-flip delay.
- **Randomization:**
  - Card icons are shuffled at the start using `Collections.shuffle()`.
- **Scoring:**
  - Calculated from remaining time or number of attempts.

---

## How to Run

### Option 1: Run in NetBeans (recommended)
1. Open NetBeans.  
2. Go to `File > Open Project...`.  
3. Choose the folder containing `MatchingGame` (with `/src`, `/nbproject`, etc.).  
4. Run the project.

Main class:
```java
matchinggame.MatchingGame
```

### Option 2: Run via Terminal
```bash
# clone the repo
git clone https://github.com/siddhipatel911/MemoryCardMatchingGame.git
cd MemoryCardMatchingGame/src

# compile
javac matchinggame/*.java

# run
java matchinggame.MatchingGame
```

---

## What I Learned:
- Building interactive GUI programs using Java Swing.
  
- Implementing timers and delayed actions for animations.
  
- Managing event-driven logic for multiple user inputs.
  
- Using randomization for unpredictable layouts.
  
- Structuring GUI projects with multiple classes and clean state resets.

---

## Future Improvements
- Add difficulty levels (easy, medium, hard).

- Add sound effects when cards match or flip.
  
- Track and save high scores.
  
- Support multiple decks or themes.
