## Add a bouncing ball

Our game of _football_ has **feet**, but no **ball!** Let’s fix that.



+ Click `Upload sprite from file`
+ Select **resources/ball.png**, and rename the sprite **ball**.
+ In the `Scripts` tab for the ball, add the following:
```blocks
    when FLAG clicked // bounce about
    broadcast [resetball v]
    forever
        move (10) steps
        if on edge, bounce
    end
```
+ Right-click on this script and click `add comment`. Add the comment **“bounce about”**.
+ Add another script to the ball:
```blocks
    when I receive [resetball v] // prepare for kick-off
    go to x: (0) y: (0)
    point in direction <pick random (1) to (360)>
```
  This tells the ball to move to the middle of the pitch for kick-off, and then point in a random direction. Why do we use `resetball`?
+ Don’t forget to add the **“prepare for kick-off”** comment, so we remember what this script does!

## Test your project

Click the green flag.

+ Does the ball move?
+ What happens when it hits the edges?
+ Are you happy with the ball speed? Try changing the `move` block to have a smaller or larger number until you’re happy with it.
+ What happens when the ball hits your players?



