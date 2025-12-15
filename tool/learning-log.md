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
* 

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
