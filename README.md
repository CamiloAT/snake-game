# Snake Game

[![Java](https://img.shields.io/badge/Java-1.8%2B-orange?logo=openjdk&logoColor=white)](https://www.java.com/)
[![Swing](https://img.shields.io/badge/UI-Swing%2FAWT-blue)](https://docs.oracle.com/javase/8/docs/technotes/guides/swing/)
[![Gson](https://img.shields.io/badge/Library-Gson%202.8.2-green)](https://github.com/google/gson)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

A classic Snake Game implementation in Java featuring persistent high scores, progressive difficulty, and a custom UI built with Swing.

---

## Gameplay Demo

<div align="center">
  <video src="https://github.com/user-attachments/assets/2d9ff34f-edbf-4c14-aad6-5c4f2aabd4b4" controls="controls" width="100%" muted="muted"></video>
</div>

---

## Main Features

- **Dynamic Difficulty System** — Three tailored levels (Easy, Medium, Hard) that modify snake length, movement speed, and spawn rates.
- **Progressive Speed** — Speed gradually increases as the snake eats, capped at a maximum limit per difficulty tier.
- **Data Persistence** — Saves game configuration and historical score data locally using JSON serialization.
- **History Dashboard** — View past game records and statistics through an intuitive history panel.
- **Information Panel** — Access game instructions and general information from the main menu.
- **Custom UI Components** — Built-in table and scroll components for a polished, consistent interface.

---

## Pages & Views

| View | Description |
|---|---|
| **MenuPanel** | Main menu with buttons to start the game, view history, and access information. |
| **GamePanel** | Active gameplay screen where the snake moves, eats food, and avoids obstacles. |
| **HistoryPanel** | Displays a table of past game records with score, date, and difficulty. |
| **InformationDialog** | Modal dialog showing game instructions and general information. |
| **ErrorDialog** | Modal dialog for displaying error messages to the user. |

---

## Execution and Development Guide

### Prerequisites

- **Java Development Kit (JDK):** Version 1.8 (Java 8) or higher

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/CamiloAT/snake-game.git
   cd snake-game
   ```

2. **Add Gson library**
   Ensure the `Libraries/gson-2.8.2.jar` file is added to your Java Build Path / Classpath.

3. **Compile and run**
   Open the project in your preferred IDE (Eclipse, IntelliJ, VS Code) and execute the main class:
   ```
   co.edu.uptc.presenter.Presenter
   ```

4. **Play the game**
   - Select a difficulty level from the main menu.
   - Use arrow keys to control the snake.
   - Eat food to grow and increase your score.
   - Avoid obstacles and the snake's own tail.

> **Note:** The game automatically saves configuration to `Files/Config.txt` and scores to `Files/Data.JSON`. Do not delete these files to preserve your progress.

---

## Project Structure

```text
snake-game/
├── src/
│   └── co/edu/uptc/
│       ├── presenter/          ← Application entry point and controller
│       │   └── Presenter.java
│       ├── model/              ← Game logic (Snake, Food, Obstacles, Score)
│       │   ├── Snake.java
│       │   ├── Food.java
│       │   ├── Obstacule.java
│       │   ├── Score.java
│       │   ├── Coordinates.java
│       │   ├── Historial.java
│       │   └── HistorialRow.java
│       ├── view/               ← UI panels and frames
│       │   ├── PrincipalFrame.java
│       │   ├── MenuPanel.java
│       │   ├── GamePanel.java
│       │   ├── SnakePanel.java
│       │   ├── ScorePanel.java
│       │   ├── FieldPanel.java
│       │   ├── HistoryPanel.java
│       │   ├── InformationDialog.java
│       │   └── ErrorDialog.java
│       ├── myComponents/       ← Custom reusable UI components
│       │   ├── MyTable.java
│       │   ├── MyTableModel.java
│       │   ├── MyTableCell.java
│       │   └── MyScroll.java
│       ├── persistence/        ← JSON data persistence
│       │   └── JsonPersistence.java
│       ├── properties/         ← Configuration management
│       │   └── Configuration.java
│       └── exceptions/         ← Custom exception handling
│           └── NotValidException.java
├── Libraries/
│   └── gson-2.8.2.jar         ← JSON serialization library
├── Files/
│   ├── Config.txt              ← Game difficulty configuration
│   └── Data.JSON               ← Historical score data
└── Images/                     ← Game assets (icons, sprites)
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 1.8+ |
| UI Framework | Java Swing / AWT |
| Data Serialization | Gson 2.8.2 (JSON) |
| Build Tool | Eclipse Java Builder / Standard JDK |
| Persistence | Local file system (TXT, JSON) |

---

## Authors

| Name | GitHub |
|---|---|
| **Camilo Andres Arias Tenjo** | [@CamiloAT](https://github.com/CamiloAT) |

*Java Game*
