# pong
Atari's 1972 classic, implemented in Lua with LÖVE

This repo is forked from games50/pong. 

Two changes are made on the repo to fit LOVE 11.3
1. In main.lua, the line love.graphics.clear(40, 45, 52, 255) has been changed to love.graphics.clear(40/255, 45/255, 52/255, 255/255). Somehow the parameters of this function now takes in scales of 0-1 instead of 0-255. https://love2d.org/wiki/love.graphics.clear
2. In push.lua, love.window.getPixelScale has been replaced with love.window.getDPIScale. https://love2d.org/wiki/love.window.getPixelScale

Aside from the incremental build of the game throughout the course, I've also added pong-ai which is a simple implementation of AI using the pong-final version. The player1 paddle will move based on the y position of ball. PADDLE_SPEED remains a constant, so the only way to beat the AI is probably to play until the speed of the ball is too fast for player1 paddle.
