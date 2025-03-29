Go to the following website:
https://github.com/caspar000/pixi-playground

Click the green "Code" button and then "Download ZIP"
![[Pasted image 20250329123928.png]]

Once the ZIP is downloaded, extract it in any location, for example Desktop.

Open the extracted folder. Open the `CMD` in the project folder. (You can do this by typing `CMD` in Windows Explorer)

After you have opened your terminal, install the required packages:
```bash
npm install
```

And run the development server with the following command
```bash
npm run dev
```

You can open the VS Code from terminal by using the following command
```bash
code .
```

Once you have opened VS Code, navigate to the file called `PixiCanvas.tsx`. This file contains the logic for drawing the game screen and Player (which is currently a cube). 
![[Pasted image 20250329124409.png]]

In this file, there are several functions which you have to implement:
1. `movePlayerLeft`
2. `movePlayerRight`
3. `movePlayerUp`
4. `movePlayerDown`
5. `movePlayerNorthWest`
6. `movePlayerNorthEast`
7. `movePlayerSouthWest`
8. `movePlayerSouthEast`

![[Pasted image 20250329125124.png]]

Each function has a comment named `// TODO`. If you get lost in the files, you can easily find these tasks by typing `TODO` in the search bar of VS Code:
![[Screenshot 2025-03-29 at 12.48.31.png]]

These functions are already associated with the buttons. You can test if these functions work correctly by clicking the buttons on the screen.
![[Pasted image 20250329124704.png]]

# Explanation
Currently, the canvas is initialized with `WIDTH = 600` and `HEIGHT = 600`. When the canvas is drawn, the pixels are drawn from the **Top Left Corner** which is (0, 0). Think of it as a coordinate system.
![[Pasted image 20250329125221.png]]

The Player (cube) also has it's own width and height. They are initialized with `WIDTH = 50` and `HEIGHT = 50`

In the beginning, the player is in the very center of the canvas. Let's denote canvas width with $C_X$ and canvas height with $C_Y$. We can denote player width with $P_X$ and player height with $P_H$. Mathematically speaking, for the player to be in the center of the canvas, his position has to be the following:
$$
\text{Position } x = \frac{C_X}{2} - \frac{P_X}{2}
$$
$$
\text{Position } y = \frac{C_Y}{2} - \frac{Y_X}{2}
$$
We divide the height and weight of the canvas to get the center point of the canvas. If we place the player at that point he will be off-center by half his width and height. We subtract half his width and half his height from the divided canvas to get the true center point for the player.

This is what it will look like if we don't take into account the width and height of the player and only place it on the center point of the canvas.
![[Pasted image 20250329130311.png]]

And this is what it should look after you subtract half of the width and height from the center point position:
![[Pasted image 20250329130605.png]]
For you to achieve movement, you have to add or subtract the player speed from the current player $x$ and $y$ coordinates:
![[Pasted image 20250329131442.png]]

Similarly for diagonal movement, where you have to increase/decrease the x and y position **at the same time**.

# TASK
Your task is to implement all the movement functions:
1. `movePlayerLeft`
2. `movePlayerRight`
3. `movePlayerUp`
4. `movePlayerDown`
5. `movePlayerNorthWest`
6. `movePlayerNorthEast`
7. `movePlayerSouthWest`
8. `movePlayerSouthEast`

While making sure that the Player cannot move out of bounds of the screen. 

## Hint
To make sure that the player does not move out of the screen, you will need a **conditional** statement, in this case, an **if statement**. With an if statement, you can run, or NOT run some code depending on the condition. The condition always evaluates to a **True** or a **False**. For example:
```javascript
a = 0
b = 1

if (a === 0) {
	console.log('This code will run because A is indeed 0')
}
if (a === 1) {
	console.log('This will not run')
}
if (b === 0) {
	console.log('This will not run')
}
if (b === 1) {
	console.log('This code will run because B is indeed 1')
}
```

The condition can have an equality `===` or inequality `!==`. For example: `if (a === 0)` will only be true when a is exactly 0. `if (a !== 0)` will be true every time that a IS NOT 0. You can also have greater than and less then, like `if (a < 0)` or `if (a > 0)`;
1. `if (a === b)` (if a is exactly equal to b)
2. `if (a !== b)` (if a is anything but b)
3. `if (a <= b)` (if a is less than or equal to b)
4. `if (a >= b)` (if a is greater than or equal to b)
5. `if (a < b)` (if a is less than b)
6. `if (a > b)` (if a is greater than b)
7. `if (a < b && c > d)` (you can have more complex statements with boolean logic (and, or, etc.))

