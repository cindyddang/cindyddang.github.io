---
layout: page
title: Snake Game
description: Personal project, Summer 2023
img: assets/img/snakegame/game_over.png
importance: 1
category: 2023
---

This is a personal project where I want to learn more about desktop application using my most comfortable program language, Java. 

Resources used:
[Original source code](https://github.com/devression/snake-game/tree/main)

Source code:
[Github Repository](https://github.com/cindyddang/Snake-Game/tree/main?tab=readme-ov-file)

The game flows:

- The snake moves automatically in its current direction.

- The player can change the snake’s direction using arrow keys.

- Each time the snake consumes food, the score increases, and the snake grows longer.

- The game ends if the snake collides with itself or the border.

Major challenge:

Collision Detection – Ensuring that the snake could detect collision with the wall

Continuous Movement – Using Timer class to create a smooth and continuous snake movement

Responsive Input Handling – Preventing the snake from reversing into itself

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/snakegame/game_play.png" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/snakegame/game_over.png" %}
    </div>
</div>
<div class="caption">
    Game play and game over screen
</div>

As this is just a small project I did during my summer while traveling, it can have a lot of more improvement, such as:

Add a Start Menu – Implement a home screen with a "Start Game" and "Exit" option because the game automatically starts when running the application

High Score Feature – Store and display the highest score achieved during gameplay.

Sound Effects – Add sound effects when the snake eats food or the game ends.