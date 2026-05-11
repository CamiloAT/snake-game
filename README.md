<div align="center">
  <h1>Snake Game</h1>
  <p><strong>A classic and dynamic Snake Game implementation in Java featuring data persistence and progressive difficulty.</strong></p>
</div>

---

## About the Project

**Snake Game** is a highly interactive desktop game developed strictly in Java. It features persistent high scores and settings, dynamic levels of difficulty, and a custom UI. The project focuses on object-oriented programming, local file management, and graphical user interfaces using Java Swing.

### Gameplay Demo

<div align="center">
  <video src="videos/Gameplay.mp4" controls="controls" width="100%" muted="muted"></video>
</div>

Developed by: **Camilo Andres Arias Tenjo**

## Key Features

*   **Dynamic Difficulty:** Three tailored levels (Easy, Medium, Hard) that directly modify the snake's initial length, movement speed, and spawn rates for both food and obstacles.
*   **Progressive Speed:** As the snake eats, its speed gradually increases frame-by-frame until reaching a maximum cap limit of 0.05s.
*   **Custom Score Strategy:** Every time the snake eats a mouse (food), the score increases by exactly one unit, regardless of the active difficulty tier.
*   **Data Persistence:** Locally saves the game configuration (`Files/Config.txt`) and historical score data (`Files/Data.JSON`).
*   **Information & History Dashboard:** Easily accessible history and general information panels via intuitive buttons located at the top right of the main menu.

## Architecture & Technologies

*   **Core Language:** Java
*   **UI Framework:** Java Swing / AWT
*   **Data Serialization:** JSON (Using Google Gson - `gson-2.8.2.jar`)
*   **Build Tool / Environment:** Eclipse Java Builder / Standard JDK

## Requirements & Installation Guide

Make sure you have the following prerequisites installed on your system before proceeding:

*   **Java Development Kit (JDK):** Version 1.8 (Java 8) is required and specifically configured for this project.

Follow these steps to run the project on your local machine:

1. **Clone or Download the repository** to your workspace directory.
2. **Setup the Library**: Ensure that the `Libraries/gson-2.8.2.jar` file is properly added to your Java Build Path / Classpath so JSON persistence can work.
3. **Compile the source code**: Use your preferred IDE (Eclipse, VS Code, IntelliJ) to build the sources in the `src/` directory.
4. **Run the Game**: Execute the main class located inside the presenter application package:
   `co.edu.uptc.presenter.Presenter`

## Difficulty Levels Specifications

### Easy Level
* **Initial Length:** 5 blocks
* **Base Movement:** 1 block per 0.8s
* **Spawn Times:** Food every 20s | Obstacles every 8s
* **Speed Progression:** Increases by 0.02s per food consumed (Max limit: 0.05s)

### Medium Level
* **Initial Length:** 4 blocks
* **Base Movement:** 1 block per 0.5s
* **Spawn Times:** Food every 10s | Obstacles every 6s
* **Speed Progression:** Increases by 0.025s per food consumed (Max limit: 0.05s)

### Hard Level
* **Initial Length:** 3 blocks
* **Base Movement:** 1 block per 0.2s
* **Spawn Times:** Food every 4s | Obstacles every 2s
* **Speed Progression:** Increases by 0.03s per food consumed (Max limit: 0.05s)

---
<div align="center">
  <i>A classic game brought to life with Java and object-oriented design.</i>
</div>
