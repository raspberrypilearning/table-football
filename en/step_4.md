## Add some more players

We can’t play a game of football with just one player! We need to add some more.



+ Create another sprite using the `Upload sprite from file` button and selecting **goalie_red.png**.
+ Change the name of the sprite to **red goalie**.
+ Drag the sprite on the stage to the right-hand side just in front of the goal.
+ Like before, grow the sprite 10 times so it is as big as the other goalie.
+ Select the **blue goalie** sprite and drag the script to **red goalie** to duplicate it.
+ Select **red goalie**, and modify the script so it looks like this:
```blocks
    when FLAG clicked
    go to x: (190) y: (0)
    forever
        if <<key [p v] pressed?> and <(y position) < [80]>> then
            change y by (5)
        end
        if <<key [l v] pressed?> and <(y position) > [-80]>> then
            change y by (-5)
        end
    end
```
  You should only have to change three things: the `y position`, and which keys are pressed.

## Test your project

Click the green flag.

+ Can you control the red goalie by pressing P and L?
+ Do the controls for the blue goalie still work?



