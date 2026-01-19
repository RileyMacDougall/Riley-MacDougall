## Jan 15 - Custom Functions & Error checking
**a)** I wrote a custom function spawnFood() to handle game mechanics and added input restrictions in keyPressed() to prevent invalid movements.
```java
// Custom Function
void spawnFood() {
  int columns = 10;
  int rows = 10;                                   
  foodX = width/4 + (int(random(columns)) * 50);
  foodY = height/8 - 25 + (int(random(rows)) * 50);
}
// Error Checking / Restriction
if (keyCode == UP && snakeDirection != 'D') snakeDirection = 'U';
```

**b)** I created `spawnFood()` to hold the code to spawn in food. Since food needs to spawn at the start of the game and every time the snake eats, it makes sense to have this logic in one reusable function. For the error checking in keyPressed, I added a restriction logic. In Snake, you cannot instantly reverse direction (e.g., if moving Down, you cannot press Up). If you did, the head would collide with the neck, causing an instant game over. 

**c)** A challenge with `spawnFood()` was keeping the food aligned with the grid. Random coordinates would place the food halfway between grid lines. I fixed this by using int(random(columns)) * 50 (since each box size is 50 x 50 pixels). This forces the food to snap exactly to the grid squares where the snake moves.
