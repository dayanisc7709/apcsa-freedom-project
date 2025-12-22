# Entry 2
##### 12/15/25

### How I've tinkered with my tool

What I've done so far is I've been able to make moving platforms and game map. There's this one [video](https://www.youtube.com/watch?v=LOhfqjmasi0) that I've been using to be able to figure out most of the stuff I've been learning and it's been really helping me out. For these new few parts that I've learned, coding still isn't really used so far. I learned that to make your entire map set up, you need something called a tilemap and a tileset. The tileset would be your selection of tiles that you're planning on using. As for the tilemap, that's the grid where your tiles will be placed in. Since I still cannot use my own art yet, I tried using the one from the video as shown. For my own custom ones, that will be used later. I wanted to focus on trying to just understand and making it look how I want it to later.

<img width="916" height="428" alt="image" src="https://github.com/user-attachments/assets/e8c34ff6-bc48-4fa8-bc75-040f2f52412d" />

Now with that, all you needed to do to draw the tiles on the map was click on your desired tile and drag it across the map. Then to switch, you would just need to repeat this small process. Another few things that had been mentioned within the video was that for bigger tiles, say if it's something like a tree, that would need multiple tiles to take up its space rather than seperate ones. But if you also would like for it have varying length, the best thing to do is have three seperate tiles. The first one can be the beginning of the tree, which would be the lower roots. Then the rest becomes obvious, the second tile is the middle of it and the last would be the end of the tree. The middle part is the one that matters mostly because it's gonna be what determines the height of the tree depending on how many times you place it. Once that's done along with the map made, it needs a physics layer, otherwise without it, the player will only fall through the map because it doesn't recognize the tiles as a solid they're supposed to be standing on. 

<img width="531" height="234" alt="image" src="https://github.com/user-attachments/assets/a6130651-7d27-47c0-b1d7-d6467f4a419a" />

I found that for certain tiles they might need a specific physics layer, something like a bridge, the layer has to be adjusted. It needs to turn to a partial collider to remove some parts of the layer and move it around a bit so that it fits perfectly on the tile. After that, I got to learn about how to make the moveable platforms to made the game more harder. A few nodes were needed, like `AnimatedBody2D`, `Sprite2D` and `CollisionShape2D`. Basically what they are is that the first one gives a body to the tiles and lets it be animated and able to collide. For the second one, it's also another body where the sprite goes so that the system knows what it is. Then the last one is what actually gives the collision to the tile. Now to actually animate it, you need another node called `AnimationPlayer`. To start, you need keyframes in order to be able to decide when and where you want your tile to move. 

<img width="966" height="192" alt="image" src="https://github.com/user-attachments/assets/9dfd472f-402d-4b26-ae16-8bc157dfde60" />

The little diamonds shown on the screen are gonna be what signifies the length of your animation. The first diamond is the beginning, so no changes are needed there. But when you place your second diamond, you need to change the position of the platform that's gonna be moving, so in this case, you would just move it to the right or left, wherver there's a seperate part to reach. Much morew can be done with this, but for now, only a simple is needed for right now. The animation only loops going in whatever direction you want it to go, so in order for that to not happen, you need to change the type of loop to be a ping pong loop. This will allow the loop to go back and forth rather than just going in one direction, then going back and repeating that.

### Winter Break FP

For this break, I hope I can make a death screen, maybe a winning screen as well, but that can come later since there's no way to win at the moment. If it's possible, I would wanna see that or maybe be able to find how to make a checkpoint so that even if the player dies, they can go back to a previous area they made it to as a milestone. I could also try finding different sources to use, so I can have more diversity with that.



[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
