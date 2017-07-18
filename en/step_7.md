## Kicking the ball

We need the ball to bounce off the players on the pitch.

+ Modify the last code block you created (**“bounce about”**) to look like this:
```blocks
    when FLAG clicked // bounce about
    broadcast [resetball v]
    forever
        move (10) steps
        if on edge, bounce
        if <<touching color [#0A9AF7]?> or <touching color [#FF0D01]?>> then
            turn cw (pick random (140) to (220)) degrees
        end
    end
```
  You should select the colours by clicking on the football players. This change makes the ball sense it is touching a player, and then bounce off them by turning (with a bit of randomness).

## Test your project

Press the green flag.

+ What happens now when the ball hits your players? Is it working for both red and blue players?



