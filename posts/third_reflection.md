## Jan 13 - Repetition Structure
**a)** I used a for loop to handle the movement of the snake's body segments.
```java
for (int i = snakeLength - 1; i > 0; i--) {       
    x[i] = x[i-1];
    y[i] = y[i-1];
}
```
**b)** The purpose of this loop is to make the snake's body follow the head. In this grid-based snake game, every segment needs to move to the position where the segment in front of it used to be. Once the first piece moves, the repetition begins and then the next piece moves, until there is no more left. 

**c)** Challenges and Solutions I initially struggled with the snake growing indefinitely. The loop worked for movement, but I had errors when the snake got too big for the array. I fixed this by capping the snakeLength variable. I also realized I needed to update the head position `x[0], y[0]` after this loop runs, ensuring the body shifts first, and then the head moves into the new empty space.
