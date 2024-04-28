# Hunger Games Text-based Simulation Game
[Back](https://abdullateefokuboye.github.io/)


![Hunger Games Image from Wikipedia](https://upload.wikimedia.org/wikipedia/en/3/39/The_Hunger_Games_cover.jpg)

## Project Context

This simulation game was created as part of my coursework in Business Analysis at Hult International Business School. It's designed to blend analytical thinking with creative problem-solving, providing a hands-on experience in strategic decision-making through programming.

## Game Overview

This game immerses players in the life of a Hunger Games tribute. Using Python, players respond to text-based prompts to make decisions that directly influence their survival. Each choice can lead to different scenarios and outcomes, enhancing the game's replayability.

![Hunger Games Arena](/pixelcut-export.jpeg)  

## Key Features

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

# Text-based Simulation Game: Hunger Games Survival

## Introduction

Dive into the world of the Hunger Games with this Python-based simulation game. Here, you'll face various challenges, make strategic decisions, and attempt to survive in a hostile environment. Let's explore how the game works, the code that powers it, and what you can do to possibly beat it.

## Game Mechanics

### Player Class

```python
import random

class Player:
    def __init__(self):
        self.health = 100
        self.strength = random.randint(5, 10)
        self.agility = random.randint(5, 10)
        self.intelligence = random.randint(5, 10)
        self.supplies = []

    def display_stats(self):
        print(f"Health: {self.health}, Strength: {self.strength}, Agility: {self.agility}, Intelligence: {self.intelligence}")
```

When a player is instantiated, they are randomly assigned strength, agility, and intelligence attributes, and their health is set to 100. These attributes will significantly influence their ability to handle the challenges ahead.

### Core Functions

#### Winning and Losing

```python
def win():
    print("You survived... at least, the first day of the Hunger Games")

def fail():
    print("Your vision starts to fade, as you begin to drift to sleep. You hear a muffled cannon sound in the distance.")
```

The `win` and `fail` functions are crucial—they define the outcomes of key game scenarios, such as combat or strategic decisions.

#### Getting Supplies

```python
def get_supplies(count):
    available_supplies = ["SWORD", "BOW", "ARROWS", "CLUB", "KNIFE", "BACKPACK", "WATER"]
    random.shuffle(available_supplies)
    print("Available supplies:", available_supplies)
    for i in range(count):
        supply = input("Type the supply you'd like to get or STOP when you are done: ").upper()
        if supply == "STOP":
            break
        elif supply in available_supplies:
            player.supplies.append(supply)
            available_supplies.remove(supply)
            print(f"You have obtained a {supply}.")
        else:
            print(f"You couldn't find {supply} and wasted time looking for it.")
```

Players can select supplies from a randomized list, crucial for survival and combat. The outcome of these selections can affect the player's chances in combat.

#### Combat Mechanics

```python
def combat():
    if "SWORD" in player.supplies or "KNIFE" in player.supplies:
        combat_strength = player.strength + 2
    else:
        combat_strength = player.strength

    enemy_strength = random.randint(3, 10)
    print("An enemy is approaching!")
    choice = input("Do you FIGHT or RUN? ").upper()
    if choice == "FIGHT" and combat_strength > enemy_strength:
        print("You successfully defeated the enemy.")
        win()
    elif choice == "RUN" and player.agility > 5:
        print("You managed to escape.")
        win()
    else:
        print("You couldn't escape or defeat the enemy.")
        fail()
```

Combat decisions hinge on the player's agility and the strength-enhancing supplies they have gathered. The player must decide to fight or flee based on their chances of success.

### Starting the Game

```python
if __name__ == "__main__":
    player = Player()
    game()
```

The game initializes by creating a `Player` object and calling the `game` function, which manages the game's flow and player interactions.

## Conclusion

The Hunger Games text-based simulation game offers an engaging and educational way to explore programming and game design. It combines basic programming concepts with game mechanics to create an interactive and fun experience.

For more information and updates, peruse the repo! [GitHub repository](https://github.com/abdullateefokuboye/The-Hunger-Games-Simulation-Game).

## Citation
Collins, S. (2008). *The Hunger Games*. First edition. New York, Scholastic Press.

[Back to homepage](https://abdullateefokuboye.github.io/)
