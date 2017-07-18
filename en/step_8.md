## GOOOOOOAAAAAALLLLLLLLL!!!!!!!!



+ Select **red goal** and add the following script:
```blocks
    when FLAG clicked // goal line technology
    forever
        if <touching [ball v]> then
            broadcast [goal v]
        end
    end
```
  This is like goal line technology - it runs all the time, checking whether the ball is touching the goal, and broadcasting a message when it is.
+ Drag the script to **blue goal** to copy it there as well.
+ Now we need to do something when **goal** is broadcast. Click `Upload sprite from file`.
+ Select **resources/goal_text.png**, and rename the sprite **goal text**.
+ Add this script to **goal text**:
```blocks
    when I receive [goal v] // goal scored
    show
    wait (1) secs
    hide
```
+ Finally, add one more script to **goal text**:
```blocks
    when FLAG clicked
    hide
```
  …to ensure the **goal text** begins the game hidden.



## Test your project

You’re ready to play a game! Press the green flag.

+ What happens when the ball goes in?
+ Try challenging a partner to a game!

## Challenge 1: Keep score

Can you add variables that will keep track of scores for the red and blue teams?

## Challenge 2: Tip the table

You might notice sometimes the ball gets stuck bouncing where the players can’t reach. Can you add a script to the ball to fix this by “tipping the table” when the spacebar is pressed?

## Challenge 3: Referee’s whistle

Can you add the sound effect **resources/whistle.mp3** so that the whistle sounds whenever a kick-off takes place?

