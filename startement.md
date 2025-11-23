# Snake Game - Project Statement

## Overview
This is a classic **Snake** game implemented in Python using the built-in `tkinter` library for the graphical user interface. The player controls a snake that grows longer when it eats food, with the goal of achieving the highest score possible without colliding with the walls or itself.

## Features
- 25×25 grid playing field (625×625 pixels)
- Smooth movement at **10 updates per second**
- Snake grows when eating red food pellets
- Score tracking displayed in the top-left corner
- Game Over screen with final score when the snake collides with walls or itself
- Arrow key controls (Up, Down, Left, Right)
- Prevention of instant reversal (you cannot go directly backwards into yourself)
- Centered game window on screen launch

## How to Play
1. Run the script (`python snake.py`)
2. Use the **arrow keys** to control the snake's direction
3. Eat the red food to grow longer and increase your score
4. Avoid running into the walls or the snake's own body
5. When the game ends, the final score is displayed in the center of the screen

## Current Limitations & Possible Improvements
- No "Play Again" functionality (game must be restarted by rerunning the script)
- Food can spawn on top of the snake's body (rare but possible)
- Fixed game speed (could be made adjustable or increase with score)
- No pause feature
- Basic visuals (could be enhanced with images, better colors, or animations)

## Future Enhancements (Ideas)
- Add a "Press any key to restart" feature after Game Over
- Increase speed gradually as score increases
- Add sound effects and background music
- High score persistence (save to file)
- Mobile-friendly touch controls (if ported)
- Different difficulty levels

## Technical Details
- **Language**: Python 3
- **Library**: `tkinter` (standard GUI library), `random`
- **Grid System**: 25×25 tiles, each 25×25 pixels
- **Game Loop**: Implemented using `window.after(100, draw)` for ~10 FPS

## Author
[ Krishna Bhumi ] – Feel free to modify and expand