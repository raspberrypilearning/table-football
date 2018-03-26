## Add a goalie

Okay – our pitch is looking good! Now let’s add some players and get them moving about.



+ Click on `Upload sprite from file` and choose **goalie_blue.png**. Rename the sprite **blue goalie**, and drag it near to the left goal.
+ Click on the `grow sprite` button, and click on the **blue goalie** sprite 10 times to scale up the sprite.
+ Click on the `Scripts` tab, and add:
```blocks
    when FLAG clicked
    go to x: (-190) y: (0)
    forever
        if <<key [q v] pressed?> and <(y position) < [80]>> then
            change y by (5)
        end
        if <<key [a v] pressed?> and <(y position) > [-80]>> then
            change y by (-5)
        end
    end
```
  Let’s look at the code.  We position the goalie, then we loop forever listening for key presses from the player. **Q** moves the goalie up, **A** moves it down. We check the `y position` of the goalie to stop it moving off the screen.

## Test your project

Click the green flag.

+ Can you control the goalie by pressing Q and A?
+ What happens when it gets to the edges of the pitch?



