## Add some attacking players



+ Create another sprite using the `Upload sprite from file` button and selecting **attack_blue.png**. Rename the sprite **blue attack**.
+ As before, grow the sprite 10 times, so the players are as big as the goalies.
+ Move the sprite into the right-hand side of the pitch, so they are attacking the red team’s goal.
+ Drag the script from **blue goalie** to **blue attack**, and modify it to match this:
```blocks
    when FLAG clicked
    go to x: (70) y: (0)
    forever
        if <<key [w v] pressed?> and <(y position) < [80]>> then
            change y by (5)
        end
        if <<key [s v] pressed?> and <(y position) > [-80]>> then
            change y by (-5)
        end
    end
```
  You should only have to change three things: the `x position`, and which keys are pressed.
+ Create one more sprite using the `Upload sprite from file` button and selecting **attack_red.png**. Rename the sprite to **red attack**.
+ As before, grow the sprite 10 times, so all the players on the pitch are the same size.
+ Move the sprite into the left-hand side of the pitch, so they are attacking the blue team’s goal.
+ Drag the script from **blue attack** to **red attack**, and modify it to match this:
```blocks
    when FLAG clicked
    go to x: (-70) y: (0)
    forever
        if <<key [o v] pressed?> and <(y position) < [80]>> then
            change y by (5)
        end
        if <<key [k v] pressed?> and <(y position) > [-80]>> then
            change y by (-5)
        end
    end
```
  You should only have to change three things: the `x position`, and which keys are pressed.

## Test your project

Click the green flag.

+ Do you have two teams of working players now? Try pressing Q, A, W and S to control the blue team, and P, L, O and K to control the red team.



