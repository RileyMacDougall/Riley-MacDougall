## Jan 14 - Arrays & Data Structures
**a)** Concept Implementation I used two arrays, x[] and y[], to store the coordinate history of the snake.
```java
int maxSnakeLength = 100;
int[] x = new int[maxSnakeLength];
int[] y = new int[maxSnakeLength];
// Accessing them in the draw loop:
for (int i = 0; i < snakeLength; i++) {      
   square(x[i], y[i], w);
}
```
**b)** I needed arrays because the snake grows constantly. I cannot create individual variables like snakeBody1, snakeBody2, etc., because I don't know how long the snake will get. Arrays allow me to store up to 100 positions (shown in int variable maxSnakeLength) using a single index i. By iterating through the array up to the current snakeLength, I can draw every segment of the snake efficiently using a simple loop.

**c)** One challenge I faced here is to get the individual pieces of the body of the snake to follow the piece before it. I fixed this problem by using arrays, being able to store a variable inside a variable. The array works so that every piece of the snake would take the piece in front of its place, every frame (except for the lead). The lead is controlled by the direction keys and creates the lead for every other piece of the snake.
