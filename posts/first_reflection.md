# Jan 9 - Variables & Data Tracking
**a)** In this project, I used several data types to manage the logic. Specifically, I used int for different values regarding integers, PImage for storing images, String for storing words, color for storing colors and char for direction handling.

For example:
```java
void mousePressed() {
  if (screen == 0) {            
    screen = 1; 
  }
```
**b)** This code is run at the start of the game to go from the title screen to the main menu. By clicking anywhere on page 0, will then change screen to page 1. Making a screen variable makes it very easy to transfer through the different screens

**c)** A challenge I faced was managing the snake's color selection. Initially, I didn't know how to pass the color choice from the menu to the game. I was going to create three different int variables for each number slot in rgb. I resolved this by creating a global color variable. When the user clicks an image in the menu, I update this variable, and the `playGame()` function reads it later to `fill()` the snake's body.
