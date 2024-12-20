# Flappy Bird Game - Java Edition

A simple, yet fun, implementation of the popular **Flappy Bird** game, created using **Java** and the **Swing** library. This version includes basic gameplay mechanics such as bird control, pipe generation, scoring, and game-over logic. It is designed to be run on any system that supports Java, making it a great project for learning Java game development concepts.

---

## Table of Contents

1. [About the Project](#about-the-project)
2. [Game Features](#game-features)
3. [How to Play](#how-to-play)
4. [Installation and Setup](#installation-and-setup)
5. [Running the Game](#running-the-game)
6. [Game Logic and Mechanics](#game-logic-and-mechanics)
7. [Project Structure](#project-structure)
8. [Screenshots](#screenshots)
9. [Customization](#customization)
10. [Credits](#credits)
11. [License](#license)

---

## About the Project

This project is a **Java** implementation of the **Flappy Bird** game that was originally developed by **Dong Nguyen**. The game allows the player to control a bird that continuously moves forward and must navigate through an endless set of pipes. The game ends when the bird collides with a pipe or falls to the ground. The objective is to achieve the highest score by avoiding obstacles for as long as possible.

The game is built using **Swing**, which provides an easy-to-use API for creating graphical user interfaces in Java. The game features basic animations for the bird and pipes, along with collision detection and a score tracking system.

---

## Game Features

- **Bird Control**: The player can control the bird's vertical movement by pressing the `Spacebar` to make it "flap" and rise.
- **Gravity Mechanics**: The bird is affected by gravity, which constantly pulls it down unless the player makes it flap.
- **Randomized Pipe Generation**: Pipes spawn at random intervals, and their height varies to create a challenging gameplay experience.
- **Score System**: The player scores points by passing through pairs of pipes. The score increases each time the bird successfully passes a set of pipes.
- **Game Over Logic**: The game ends when the bird collides with a pipe or falls to the bottom of the screen.
- **Restart Capability**: After losing the game, the player can restart the game by pressing the `Spacebar` again.
- **Smooth Animations**: The bird and pipes are rendered with smooth animations, enhancing the gaming experience.

---

## How to Play

1. **Launch the Game**: To start the game, run the `App.java` class. This will launch the game window.
2. **Flap to Fly**: Press the `Spacebar` to make the bird flap its wings and move upward. Release the `Spacebar` to allow gravity to pull the bird downward.
3. **Avoid Obstacles**: The bird must fly through the gaps between pipes. Avoid colliding with the pipes or falling to the ground, as this will end the game.
4. **Score**: Each time the bird successfully passes through a pair of pipes, the score increases by 0.5 points.
5. **Game Over**: If the bird hits a pipe or falls off the screen, the game ends, and the final score will be displayed.
6. **Restart**: After the game is over, press the `Spacebar` to restart the game.

---

## Installation and Setup

To run this game on your local machine, you’ll need to have **Java** installed. The game is developed using **Java 8** or later, so make sure to install an appropriate version of the Java Development Kit (JDK).

### Prerequisites

- **Java Development Kit (JDK)**: Version 8 or later. Download it from [Oracle's official website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).
- **IDE/Editor**: You can use any Java-compatible Integrated Development Environment (IDE) or a simple text editor with terminal commands. Popular choices include:
  - IntelliJ IDEA
  - Eclipse
  - VS Code (with Java extensions)

### Steps to Install

1. **Clone the Repository**: First, clone the repository to your local machine using the following command:
   ```bash
   git clone https://github.com/yourusername/flappy-bird-java.git
   ```
   Replace `yourusername` with your actual GitHub username.

2. **Navigate to the Project Folder**:
   ```bash
   cd flappy-bird-java
   ```

3. **Compile the Java Code**:
   If you're using the terminal, compile the `App.java` and `FlappyBird.java` files with the following command:
   ```bash
   javac App.java FlappyBird.java
   ```

4. **Ensure Images are in the Right Place**: Make sure you have the following images in the same directory as the `.java` files:
   - `flappybirdbg.png` (Background image)
   - `flappybird.png` (Bird image)
   - `toppipe.png` (Top pipe image)
   - `bottompipe.png` (Bottom pipe image)

   If the images are not included, the game will not load the images correctly.

---

## Running the Game

Once the setup is complete, you can run the game with the following command:

```bash
java App
```

This will launch the game in a window, and you can start playing by pressing the `Spacebar` to make the bird flap.

---

## Game Logic and Mechanics

### Bird Movement and Gravity

- The bird starts at the center of the screen and is affected by gravity, which pulls it down with a constant velocity (`gravity` variable).
- When the player presses the `Spacebar`, the bird's vertical velocity (`velocityY`) is set to a negative value, causing the bird to "jump" or flap upward.
- The bird's position is updated continuously as the game loop runs, with the `velocityY` being incremented by `gravity`.

### Pipe Generation

- Pipes are generated at regular intervals (every 1500 milliseconds) and appear at random vertical positions.
- Each pipe consists of a top pipe (`toppipe.png`) and a bottom pipe (`bottompipe.png`), with a gap between them through which the bird must fly.
- The pipes move horizontally towards the bird, and if the bird passes through a pipe (without hitting it), the score increases.

### Collision Detection

- The game checks for collisions between the bird and the pipes. If the bird’s area intersects with a pipe’s area, the game ends.
- Additionally, if the bird falls below the screen (y-coordinate exceeds the board height), the game ends.

### Score System

- For each pair of pipes that the bird successfully passes through, the score increases by 0.5 points.
- The score is displayed in the top-left corner of the screen.

### Game Over and Restart

- The game ends if the bird collides with a pipe or falls off the screen. At this point, the final score is shown.
- The player can restart the game by pressing the `Spacebar` after the game ends.

---

## Project Structure

The project is structured as follows:

```
flappy-bird-java/
│
├── App.java               # Main class that runs the game
├── FlappyBird.java        # Class that defines the game logic and rendering
├── flappybirdbg.png       # Background image for the game
├── flappybird.png         # Image of the bird
├── toppipe.png            # Image of the top pipe
├── bottompipe.png         # Image of the bottom pipe
└── README.md              # This file
```

---

## Screenshots

Here are some screenshots of the game in action:

![Flappy Bird Screenshot](screenshots/flappybird1.png)
*The bird flying between pipes.*

![Flappy Bird Game Over](screenshots/flappybird2.png)
*The game over screen with the final score.*

---

## Customization

You can customize the game by modifying the following:

- **Images**: Replace the default images (`flappybirdbg.png`, `flappybird.png`, `toppipe.png`, `bottompipe.png`) with your own assets to change the look and feel of the game.
- **Difficulty**: Adjust the `placePipeTimer` and `velocityY` to modify the speed at which pipes spawn and how the bird moves.
- **Score System**: Modify the score increment and display logic to change how the score is calculated or shown.

---

## Credits

- **Author**: Sitender Narwal
- **Images**: The images used in this project are placeholders. You can replace them with your own custom images or use free resources online.
- **Inspiration**: This game is based on the original Flappy Bird game developed by **Dong Nguyen**.

---
