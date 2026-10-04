# Logic Gate Bouncer (Pure Logic Gates, Simulated)

A bouncing ball built entirely from logic gates. It does not use any
microcontroller. Runs in the Digital logic simulator. Built for fun when I
was in 5th grade.

I originally wanted to make Ping Pong out of straight logic gates, but it
was too hard. Trying to build one led me to build my first CPU, which is in
another one of my repositories.

## How it works
The ball's position is tracked by two counters, one for X and one for Y.
Each counter can count up or down. When the ball hits a wall, the matching
counter switches direction. For example, if the Y counter was counting up
and the ball hits the top wall, it starts counting down instead. That
reversal is the bounce.

It works, but it has a bug, sometimes the ball jumps instead of moving
smoothly. My guess is that the direction change and the count step happen
on the same clock edge, so the counter steps the wrong way right at the
wall.

## Versions
- **Original, V2, V3, V4:** Each one builds on the last on the way to V5. None of them work properly.
- **V5:** The working version. The ball bounces off all the walls, but it still has the jump bug.
- **V6:** An attempt at adding a paddle. The display is an LED matrix, and I couldn't get control over where the paddle lights up. The result is a paddle that flashes at a low frame rate and follows the ball, so it never misses.

## Running it
1. Download and install [Digital](https://github.com/hneemann/Digital).
2. Download this repository.
3. Open the dig file you want in Digital. Use V5 for the best working version.
4. Press the start button.

## Alternative
If you dont want to download the simulator there are images in the img folder but you have to download the image to zoom in and see it clearer.

## Credits
Built and simulated with [Digital](https://github.com/hneemann/Digital),
the digital logic designer and circuit simulator by Helmut Neemann (hneemann).

## License
MIT
