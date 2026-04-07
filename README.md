# Alien Invasion 👾

A feature-rich, 2-D arcade shooter built with **Python** and the **Pygame** library. This project implements a modular, object-oriented approach to game development, featuring dynamic difficulty scaling, state management, and real-time collision physics.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pygame](https://img.shields.io/badge/Library-Pygame-green.svg)

## 🚀 Overview

The player controls a ship at the bottom center of the screen. The goal is to shoot down a fleet of aliens that move horizontally and drop down as they reach the screen edges. As the player clears waves, the game speed increases, providing a progressively challenging experience.

## 🛠️ Technical Architecture

The project is built using a **Modular Monolith** pattern, ensuring that each game component is encapsulated within its own class/module.

### Key Components:

- **`alien_invasion.py`**: The central orchestrator. It manages the main game loop, event handling (keyboard/mouse), and coordinates interactions between sprites.
- **`settings.py`**: A centralized configuration hub. This allows for global adjustments to game speed, screen dimensions, and scoring without digging into core logic.
- **`ship.py` / `alien.py` / `bullet.py`**: These utilize **Pygame Sprites**, allowing for efficient group management and collision detection using `pygame.sprite.Group`.
- **`game_stats.py` / `scoreboard.py`**: Handles persistence of session data and real-time rendering of UI elements (Score, High Score, Level, and Ships Remaining).

## ✨ Features

- **Dynamic Difficulty:** Utilizes an `increase_speed` algorithm that scales the velocity of aliens and bullets as levels progress.
- **Collision Physics:** Implements `sprite.groupcollide` and `sprite.spritecollideany` for precise hit-box detection.
- **Responsive Control:** Low-latency movement logic using `KEYDOWN` and `KEYUP` event flagging.
- **State Management:** Distinct game states (Active vs. Inactive) with a clickable "Play" button and mouse-visibility toggling.

## 📥 Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/alien-invasion.git](https://github.com/yourusername/alien-invasion.git)
   cd alien-invasion
   Install dependencies:
   ```

Bash

pip install pygame
🎮 How to Play
Run the main game file:

Bash

python alien_invasion.py
Controls:
Left/Right Arrows: Move ship.

Spacebar: Fire bullets.

Q: Quit game.

📜 Credits
This project was developed based on the Python Crash Course curriculum by Eric Matthes, featuring custom architectural refinements for state management and UI.

Author: Aman Pausker

---
