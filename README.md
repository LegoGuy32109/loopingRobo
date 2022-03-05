# loopingRobo
Dynamic 3D model assignment for Advanced Game Developmet

![](ezgif.com-gif-maker.gif)

Checkout the .mp4 for a clearer video of the render.

## This Project Contains:
* A Robot with a combined procedural and painted texture (for rust!)
* An armature puppeting the robot mesh for animation
* Sculted terrain in a circle for the loop, along with a grass texture applied
* procedural textures on the path and treads of the robot
* A custom enviroment texture with HDRI and gradient background.
* Muliple properties animated like, material on robot's chest, rotation of world, camera angle, position of robot, as well as armature animations.

## What did I learn?
How to animate armatures, as well as flip animation poses with `Ctrl-Shift-V`, very convenient for a 2 pose animation. To get that flipped pose paste to work, I had to reset the roll on the bones, or else I would have a arm going in front or backwards. Thanks to the command `Clear Roll` that problem solved it. I also learned how to weight paint the verticies on the robot mesh, specifically the head. I wanted the head bone to move the entire head but it had reduced weight at the top of the head, so it would stretch weirdly. You have to select the armature, and then the object and switch into weight paint mode to actually see the bone you're trying to edit. Luckily I figured that out, and now the whole head animates. 

I was trying to use modifiers to curve a flat landscape around a curve object, but that still had bumps like I was making a hexagon rather than a circle for the looping terrain. I discovered the easier approach was to make a high detained cylinder, then delete 2/3s of it, model the terrain on that 1/3, then duplicate it around the origin and merge with the original 1/3d.

Animating using the timeline is very convenient, I never had to edit the node graph or anything thanks to the ability to right-click and select linear-interpolation over things like world rotation so it would loop perfectly. I had some experience animating going into this project but I enjoyed animating more propoerties then I had before, like the material on the robot's chest turning black animating a flicker effect. The timeline also makes it easy to offset animations so multiple things are happening at different intervalls, and you can find the interval you want selecting the whole animation for a property and moving it around until you find the perfect movement.

Another thing! Prof Harris when you get in that weird circle select mode you can't get out of, press `W` until you're back to the tweak tool. I fixed the problem by unbounding the W keybind for the ToolBar and the 3D view. I don't know which one actually does it so I did both to be safe. Probably the most useful information I learned during this project.

## Here is my node graph for the world texture:
![image](https://user-images.githubusercontent.com/37216503/156860237-a2017c24-4b75-4a10-ac3a-cdc985a71fb1.png)
## Here is the node graph for my robot combining procedural and painted textures:
![image](https://user-images.githubusercontent.com/37216503/156860170-f4052cee-b64f-4e13-a0db-87ce64bbb7af.png)

# Biggest Takeaway
If you want to make a looping animation, use linear interpolation. You don't need it for everything, I still have beizer for the robot hand movements, but the moving background especially requires it for it to look good looping. This project had me complete my first perfect loop and I am very proud of that milestone.

