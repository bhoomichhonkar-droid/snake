# snake
#  Python Snake Game

A classic **Snake Game** implemented in Python using the **Tkinter** library for the graphical user interface.

##  Features

* **Classic Gameplay:** Control the snake, eat the food, and grow its length.
* **Collision Detection:** Game over upon hitting the boundaries or colliding with the snake's own body.
* **Score Tracking:** Displays the current score based on the amount of food consumed.
* **Responsive Control:** Uses arrow keys for smooth direction changes.
* **Simple GUI:** A clean, black canvas interface built with Tkinter.

##  How to Run

### Prerequisites

You need **Python 3.x** installed on your system. The game uses the standard `tkinter` library, which is typically included with most Python distributions.

### Execution

1.  **Save the Code:** Save the provided Python script as `snake.py`.
2.  **Run from Terminal:** Open your terminal or command prompt, navigate to the directory where you saved `snake.py`, and run the following command:

    ```bash
    python snake.py
    ```

3.  **Start Playing!**

##  Controls

The game uses the standard arrow keys for controlling the snake's direction.

| Key | Action |
| :--- | :--- |
| **↑** (Up Arrow) | Move Up |
| **↓** (Down Arrow) | Move Down |
| **←** (Left Arrow) | Move Left |
| **→** (Right Arrow) | Move Right |

**Note:** You cannot reverse the snake's direction instantly (e.g., if moving right, pressing left will be ignored).

## 📐 Game Mechanics and Customization

The core game parameters are defined at the beginning of the script:

| Variable | Description | Default Value |
| :--- | :--- | :--- |
| `ROWS` | Number of grid rows. | `25` |
| `COLS` | Number of grid columns. | `25` |
| `TILE_SIZE` | Size of each grid tile (in pixels). | `25` |

You can modify these variables to change the size of the playing field and the snake's movement size.

* The **game speed** is controlled by the `window.after(100, draw)` call in the `draw()` function. `100` milliseconds corresponds to **10 Frames Per Second (FPS)**. Decreasing this number (e.g., to `50`) will make the game faster.

##  Future Improvements (To-Do)

* Implement a **Game Restart** feature after "Game Over."
* Add different **difficulty levels** by adjusting the speed.
* Incorporate **sound effects** for eating food and game over.
* Improve **food placement** logic to ensure it doesn't spawn on the snake's body.
* Implement a **high-score** persistence mechanism.

##  Code Structure Highlights

The game is structured around a simple `Tile` class and a main game loop managed by Tkinter's `window.after()`.

* **`Tile` Class:** A basic class to represent the position of the snake's head, body segments, and the food.
* **`change_direction(e)`:** Handles user input from key presses, ensuring the snake cannot immediately reverse.
* **`move()`:** The main physics and logic update function, handling:
    * Updating the snake's position.
    * Moving the body segments.
    * Checking for **wall and self-collision** (Game Over conditions).
    * Handling **food collision** and spawning new food.
* **`draw()`:** The rendering function, which:
    * Calls `move()`.
    * Clears the canvas (`canvas.delete("all")`).
    * Draws the food and all snake segments.
    * Displays the score or the "Game Over" message.
    * Schedules the next call via `window.after()`.

---

*I can also help you implement the "Game Restart" feature you noted in the `change_direction` function if you'd like!*
