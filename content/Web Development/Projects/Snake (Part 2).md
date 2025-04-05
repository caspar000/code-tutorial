In this homework, you will implement correct movement for the game "Snake".

[Snake Project GitHub](https://github.com/caspar000/pixi-playground)

# Explanation
I have changed the previous implementation to be closer to what "Snake" should look like. There are now only 4 movement directions (up, down, left, right). Instead of pressing the buttons repeatedly to get a movement update, I have implemented an update function which will move the player in the direction that he is currently moving. This direction is saved in the `playerDirection` variable and is changed when you click on the UI buttons or press the movement keys: (w, a, s, d)

![[Pasted image 20250405125224.png]]


# Task
Implement the following movement functions. You have to write conditional statements so that the player does not move out of bounds of the screen.
![[Pasted image 20250405125847.png]]

Pressing the UI Buttons or W, A, S, D will run the following function:
![[Pasted image 20250405130022.png]]

You have to modify it so that the player cannot move in the opposite direction. E.g., if the player is moving UP he cannot change direction to DOWN; if he is moving LEFT he cannot change the direction to RIGHT, etc. 

TIP: This could be accomplished with multiple if statements or a single switch statement.

# Reminders
You can run the development server with:
```bash
npm run dev
```