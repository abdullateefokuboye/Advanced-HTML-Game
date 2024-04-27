# Hunger Games Text-based Simulation Game
![Hunger Games Image from Wikipedia](https://upload.wikimedia.org/wikipedia/en/3/39/The_Hunger_Games_cover.jpg)
## Introduction

Experience the thrill and strategic challenge of the Hunger Games with this text-based Python simulation game. Step into the shoes of a tribute, make critical survival decisions, and navigate the complexities of the arena.

## Project Context

This simulation game was created as part of my coursework in Business Analysis at Hult International Business School. It's designed to blend analytical thinking with creative problem-solving, providing a hands-on experience in strategic decision-making through programming.

## Game Overview

This game immerses players in the life of a Hunger Games tribute. Using Python, players respond to text-based prompts to make decisions that directly influence their survival. Each choice can lead to different scenarios and outcomes, enhancing the game's replayability.

![Hunger Games Arena](https://static.wikia.nocookie.net/thehungergames/images/c/c3/Arena_75th.png/revision/latest?cb=20131029043339)  

## Key Features

### Initial Setup

At the start of the game, players are initialized with specific attributes such as health, strength, and intelligence that influence their performance throughout the game.

```python
def initialize_player(health, strength, intelligence):
    return {
        'health': health,
        'strength': strength,
        'intelligence': intelligence,
        'inventory': []
    }
```
*Initializes the player with health, strength, intelligence, and an empty inventory.*

### Decision Making

Players choose their actions, each affecting their survival odds. Here’s how players can interact with the game:

```python
def choose_action(player):
    print("Choose your action:")
    print("1. Search for food")
    print("2. Hunt")
    print("3. Hide")
    action = input("> ")
    if action == '1':
        search_for_food(player)
    elif action == '2':
        hunt(player)
    elif action == '3':
        hide(player)
    else:
        print("Invalid action")
        choose_action(player)
```
*Prompts player to choose an action and processes the input.*

### Game Dynamics

The game's mechanics include managing resources, maintaining health, and making strategic decisions to survive each day in the arena.

## Features
- **Text-based Interaction**: Simple text-based gameplay allows for an engaging storytelling experience.
- **Multiple Decision Paths**: Players can choose different strategies for survival, each with unique challenges and outcomes.
- **Dynamic Content**: Based on the player's choices, different scenarios unfold, making each gameplay experience unique.

## Technologies Used
- Python: The game logic is implemented using Python, making use of functions, loops, and conditional statements to drive the gameplay.

## Game Mechanics
- **Decision Making**: Key to surviving in the game. Each choice can lead to different outcomes.
- **Resource Management**: Players decide which supplies to gather, impacting their ability to survive.

## Conclusion

The Hunger Games text-based simulation game offers an engaging and educational way to explore programming and game design. It combines basic programming concepts with game mechanics to create an interactive and fun experience.

For more information and updates, peruse the repo! [GitHub repository](https://github.com/abdullateefokuboye/The-Hunger-Games-Simulation-Game).

## Citation
Collins, S. (2008). *The Hunger Games*. First edition. New York, Scholastic Press.
