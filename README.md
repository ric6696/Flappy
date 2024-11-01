# Flappy Bird
Project Assignment: Build Flappy Bird!

<img width="340" alt="Screenshot 2024-11-01 at 4 31 13 PM" src="https://github.com/user-attachments/assets/0a46cd8a-91e3-4d8b-95b0-5c667bc17662">


## 1. Introduction

Flappy Bird is a simple yet challenging game that has captured the hearts of millions around the world.

In Flappy Bird, players are tasked with guiding a delightful bird to fly through a series of obstacles. The objective is clear: fly through as many obstacles as possible without colliding with them, falling to the ground or hitting the ceiling.

Each successful pass earns the player a point, contributing to their overall score. In this project, you will implement Flappy Bird with MIPS assembly program.

## 2. Game Rules

The game window is represented as a grid, with the x-axis and y-axis aligned with the horizontal and vertical directions, respectively. The origin is located at the top left corner of the game window. Moving from the origin, the x-coordinate increases towards the right, while the y-coordinate increases towards the bottom.

## 3. Game Control

In the world of Flappy Bird, certain physical principles are simulated, such as a constant acceleration due to gravity that affects the falling velocity of the bird.

Let’s review some basic physics concepts from secondary school. Suppose an object has a velocity, v, measured in meters per second (m/s). On Earth, the acceleration due to gravity is approximately 9.8m/s2. If the object starts falling t seconds ago, its current falling velocity can be calculated using the formula v = g × t. In Flappy Bird, the value of g is set to 1.

However, in Flappy Bird, distance is measured in pixels rather than meters, and time is measured in game loops rather than seconds. The velocity and position of the bird are updated once every two game loops, so two game loops correspond to one time unit of the bird’s movement.
In addition to free fall, the bird can also fly. The bird’s flying operation is con- trolled by the player’s mouse. Clicking the mouse makes the bird fly upwards by setting its velocity to -9. The negative value indicates that the bird is moving upwards rather than falling. When the mouse is released, gravity starts acting on the bird again.

Let’s consider a simple example of how the bird ascends and falls. Suppose the bird starts with a velocity (v) of 14 and is initially positioned at y = 548. After two game loops (1 time unit) have passed, the v becomes 15 (vi+1 = vi + g ∗ t = 14+1∗1),andthebird’spositionisupdatedtoy=563(yi+1 =yi+v).After one more time unit, v = 16 and y = 579. Suppose after one additional time unit, you click the mouse, resulting in v = −9 and y = 570. If you continue to press the mouse button for another time unit, the velocity remains -9, and the position becomes y = 561. For subsequent time units, if you release the mouse, the velocity and position change as follows: (v = −8, y = 553), (v = −7, y = 546), (v = −6, y = 540), and so on. At this point, the bird is still moving upward, but its velocity decreases with each time unit. When the velocity reaches 0, the bird starts to fall again.

