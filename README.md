# Chapter 8: Introduction to Pygame

## Overview

This chapter introduces **Pygame**, a Python library used to create
games and multimedia applications. It provides tools for handling
graphics, keyboard input, sounds, and game loops.

With Pygame, developers can create simple games such as puzzles, arcade
games, or simulations while learning important game development
concepts.

------------------------------------------------------------------------

# 8.1 Overview of Game Development Concepts

Before creating a game, it is important to understand some basic
concepts used in most games.

### Game Window

The game window is the area where the game graphics are displayed. It is
created when the program starts.

### Game Loop

The game loop is the **core of every game**. It continuously runs while
the game is active and is responsible for: - Checking player input
(keyboard, mouse) - Updating the game state - Drawing graphics on the
screen

### Frame Rate

Frame rate determines **how many times the screen updates per second**.
A common frame rate is **60 frames per second (FPS)** for smooth
gameplay.

### Events

Events include actions such as: - Pressing a key - Moving the mouse -
Closing the game window

Pygame listens to these events so the game can react to user actions.

------------------------------------------------------------------------

# 8.2 Installing and Setting Up Pygame

Before using Pygame, it must be installed.

### Step 1: Install Pygame

Run this command in the terminal or command prompt:

``` bash
pip install pygame
```

### Step 2: Import Pygame in Python

``` python
import pygame
```

### Step 3: Initialize Pygame

``` python
pygame.init()
```

Initialization prepares the modules needed for graphics, sound, and
input handling.

------------------------------------------------------------------------

# 8.3 Understanding the Main Game Loop

The **main game loop** keeps the game running until the player exits.

It usually performs three main tasks:

1.  **Handle Events** -- Detect player input
2.  **Update Game Logic** -- Update positions or states
3.  **Render Graphics** -- Draw objects on the screen

The loop continues until the player closes the game window.

Example structure:

``` python
running = True

while running:
    # Check events
    # Update game logic
    # Draw graphics
```

------------------------------------------------------------------------

# 8.4 Displaying the Game Window and Setting the Frame Rate

To create a game window, we define the window size and display it using
Pygame.

We also control the frame rate using a **Clock object**.

------------------------------------------------------------------------

# Example: Simple Pygame Window

The following program opens a window and keeps it running until the user
closes it.

``` python
import pygame
import sys

# Initialize pygame
pygame.init()

# Create game window
width = 800
height = 600
screen = pygame.display.set_mode((width, height))

# Set window title
pygame.display.set_caption("My First Pygame Window")

# Create clock for frame rate
clock = pygame.time.Clock()

running = True

while running:

    # Check events
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Fill screen with color
    screen.fill((0, 120, 200))

    # Update display
    pygame.display.flip()

    # Set frame rate (60 FPS)
    clock.tick(60)

# Quit pygame
pygame.quit()
sys.exit()
```

------------------------------------------------------------------------

# How the Code Works

1.  **pygame.init()** initializes the Pygame library.
2.  **pygame.display.set_mode()** creates the game window.
3.  **pygame.event.get()** detects events like closing the window.
4.  **screen.fill()** fills the screen with a background color.
5.  **pygame.display.flip()** updates the screen.
6.  **clock.tick(60)** limits the game to 60 frames per second.

------------------------------------------------------------------------

# Summary

In this chapter, we learned:

-   The basic concepts of **game development**
-   How to **install and set up Pygame**
-   The importance of the **main game loop**
-   How to **create a game window and control frame rate**

These fundamentals are the first steps in building interactive games
using Python.
