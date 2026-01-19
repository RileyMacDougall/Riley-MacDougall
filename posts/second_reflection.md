## Jan 12 - Selection Structure
**a)** I used if and else if statements to handle collision detection. This logic determines if the snake has moved outside the boundaries of the game board.

if (snakeHeadX < width/4 || snakeHeadX >= width/4 + width/2 ||  
    snakeHeadY < height/8 - 25 || snakeHeadY >= (height/8 - 25) + width/2) {
      screen = 3; }

**b)** The purpose of this decision structure is to enforce the rules of the game: if the player hits a wall, they lose. I implemented it this way by comparing the snakeHeadX and snakeHeadY against the specific pixel coordinates of the board (which is smaller than the full window). If any of these conditions are true (meaning it is true that the head is out of bounds), the program immediately changes screen to 3, switching the screen to the "Game Over" page.

**c)** The main challenge was that my game board is centered inside a decorative frame, not the whole canvas. At first, I just checked against 0 and width, but the snake would float over the wooden border. I fixed this by calculating the specific margins (e.g., width/4) and adding the offset (height/8 - 25) to ensure the collision triggered exactly at the visual edge of the grid.
