# Tool Learning Log

## Tool: **Godot**

## Project: **2D game with favorite media that involves horror or adventure elements**

---

### 12/12/25:
* Learning from this video: https://www.youtube.com/watch?v=LOhfqjmasi0
* Tileset is a collection of tiles that are created to be used to create tiles/map for the game
* Tilemap is where you can put the tileset to use and build your game world
* If there's a big tile you need, you can erase the spots where it says it's seperate tiles and go to array mode
* Array mode will recgonize more than two tiles as one big tile
* You're able to set it up so that the tiles can have varying length as well
  
<img width="100" height="125" alt="image" src="https://github.com/user-attachments/assets/81c5021d-2b54-44d9-9d27-78b8de084c8d" />

* If there's something like a tree, there can be three different tiles set up as the tree and you would only need those because the middle tile will conclude the height of it
* Multiple tiles are able to be selected at once to place them in the same area on the map
* With select mode, you can pick out many tiles on the map and be able to move them around
* Once tilemap is finished, it will need a physics layer for the player
* Without it, our player falls down since it doesn't recgonize the tiles as something solid to stand on yet
* Once applied, you can choose which tiles need the layer, so things like obstacles aren't included with the physics
* Other things such as bridges will need a partial collider

  <img width="531" height="234" alt="image" src="https://github.com/user-attachments/assets/6c732bfb-4a89-4e09-9465-dae0760eea6c" />

* The physics layer can be moved around at different angles to make sure it hits the object
* Has to be precise or else there's an error and player gets stuck between objects
* With long tilemap, the camera won't follow player yet
* Camera2D has to be placed in a group under the player so it will follow them
* To make sure, there has to be a cross in the middle of the player
* Position smoothing has to be enabled in order for camera view to be smoother
* Next time I wanna try adding moving obstacles
* For another time, how do you add collectable items like coins?

### 12/14/25:
* Same video as from before, has a lot of helpful steps to learn from
* Learned how to make moveable platforms
* AnimatabledBody2D - Physics body that will allow us to animate a node and still be able to collide
* Sprite2D - Will create a body to place your sprite in
* Will have to be placed as a sprite so that the objects are able to be moved
* CollisionShape2D - Add a collision to a 2D shape
* One way collision enabled will allow your platform to be able to hop onto it but only from one direction

  <img width="83" height="94" alt="image" src="https://github.com/user-attachments/assets/b5ffc7ba-d2d9-48da-be96-e0006f7ee357" />

* The direction the arrow faces is the direction that the player isn't able to pass through it
* If it goes up, it will pass, it goes down, it can't pass through it
* Changing z-index of the player to be higher than the others will allow for it to be shown in front of the player
* AnimationPlayer will actually let you animate the platform so it moves side to side
* Many keys pop up on the side, which represents keyframes
* Clicking the one next to position is the one that lets it move side to side
* What happens if you click the others and what do they do?
* If animation only goes to one direction, clicking loop will only make it go that way
* Ping-pong loop allows for it to go back to back, like the name suggests
* The length of this can be changed by moving keyframe

<img width="966" height="192" alt="image" src="https://github.com/user-attachments/assets/1ea0f76c-d1e8-4629-ac54-f77083d8e2dd" />

* Area2D - Type of node used when you don't want to collide w/ other objects, but just detect collisions
* AnimatedSprite2D - Node used to allow you to animate your sprites
* Collectable item will need a CollisionShape2D as well
* Script needs to be added inorder for player to pick up coin
* Clicking the collectable item, then node will show the many built-in signals you can use
* Body_entered - Signal that is triggered when physics body touches area
* When checking for collisions, it will check for every body rather than just the players
* The player's physics layer number can be changed to prevent this
  
* <img width="397" height="244" alt="image" src="https://github.com/user-attachments/assets/076b24d2-ac71-4b08-9fd3-9e0a9730ce09" />

* For the item, the mask layer number will be needed to be changed instead
* With that, it will only detect collisions from player
* Adding the `queue_Free()` function will remove the item from the map
* For next time, I want to be able to add scores, how to respawn or a spawnpoint
* I also wonder if this is finally where I'll have to do coding?

  ### 1/2/26

* From the video, we're learning how to deal with player falling out map and dying
* Camera can have a limit of where it can and can't go
* If the limit is trying to be surpassed, the camera won't move until it goes back within bounds
* Useful for if the plauer dies, the camera won't be stuck in an infinite loop of going down
* To make the player actually die, there needs to be a kill zone
* A new scene needs to be created in order to do this
* This kill zone now needs a shape so that it knows when it's collided with it
* Once shape is added, it will need a script so that it does as it's meant to

<img width="1003" height="260" alt="Screenshot 2026-01-04 223329" src="https://github.com/user-attachments/assets/65ed90c2-882b-4ae6-a69f-dde388c4d5c5" />

* A timer is needed so that it adds some delay before restarting
* When timer runs out, it will need more code for it to make an action
* Once timer has no more time on the clock, it will reload the scene
* Order of what happens with the script:
  * Condition for it to work it that player enters kiil zone
  * Death message appears on screen
  * Timer starts going
  * When over, scene reloads
  * Restarts game and it respawns the player
 
<img width="411" height="305" alt="Screenshot 2026-01-04 225025" src="https://github.com/user-attachments/assets/b47d92ee-ee7f-44a1-a3fb-fb7ed37a28e5" />

* This ended up being the entire script for it
* I wonder how you can decorate the death screen or add stuff to it?
* Maybe a button to be able to restart in the future rather than having a timer for it
* For next time, I want to see how you would be able to make a checkpoint

  ### 1/3/26
  

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
