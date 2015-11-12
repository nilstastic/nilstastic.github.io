---
layout:     post
title:      V^Bert - a retrospective
date:       2013-09-11 15:31:19
image:		qbert.png
summary:    I’ve always liked a challenge, and since I’m not a smart man these things seem to present themselves quite often. This time it was in the form of the Oculus/Indiecade VR Jam and I instantly knew that it was to interesting to pass up. After doing some research..
categories: oculus_rift
---

I’ve always liked a challenge, and since I’m not a smart man these things seem to present themselves quite often. This time it was in the form of the Oculus/Indiecade VR Jam and I instantly knew that it was to interesting to pass up. After doing some research it seemed that almost everyone was going with a game engine like Unity or UDK, but since I like to know how stuff works, this was not an option.

##The game
<img src="/images/qbert.png" style="float:right">
But let’s start with was actually accomplished. V^bert is a game heavily inspired by the classic arcade game Q*Bert from the early 80′s. What makes Q*Bert such a good inspiration is that it is set in one of the first isometric worlds and it was just begging for a VR adaption.

The player starts out in a room containing a single arcade machine – V^Bert. When [enter] is pressed the player is transported into the actual game. The transportation sequence also gives the user some time to familiarize themselves with the world inside the arcade.

The rules of V^Bert are quite simple.
 - Jump on each box to change its color
 - Avoid the snakes and the blobs
 - Do no jump off the edge!

When all the boxes have been hit a new level is loaded. The second level requires the player to jump on each box twice while the third and final level makes the boxes disappear one by one – which makes it a lot more exciting. When the final level is complete the player finds him or herself standing on a single box in the middle of space. A single powerful jump initiates the ending sequence – but more about that later. =)

##The good
Learning something from scratch is always an interesting experience and I knew that if I ever wanted to be able to do restraint-free development I needed to get my act in order and get to work. I started by doing some research and with stackoverflow as my guide I figured out what libraries I needed to use to get where I wanted to go.

 - C++
 - OpenGL
 - Bullet Physics
 - Oculus SDK
 - Assimp
 - DevIL

###C++ hell
Ignoring the fact that my C++ experience was measured in days instead of years I went forth into the great unknown – and to my surprise it actually worked! Getting Visual Studio to link the GLFW library was hell, but the good thing about experience is that it adds up. Linking and getting up to speed with DevIL and Assimp to load my first model (a box created in blender) was only hard and when I got to the point where I had to use Bullet Physics to actually create my world and the Oculus SDK to look around I felt quite comfortable with using source archives, building and linking.


###Jump!
The first thing I got working was basic jumping with the keyboard, but it felt quite boring. That changed on a late night when I tried to use the accelerometer in the Rift to trigger the jump – and it worked wonderfully! After some tweaking where I had to take data from the orientation of the Rift into consideration I ended up with a great jumping experience. I briefly experimented with adjusting the jumplength so that the player could jump 2 blocks but I quickly decided that it was not in the spirit of the 80′s and moved on. =)

###Assets and blender
As I started creating the assets for the game I quickly learned that Blender is not the horrible piece of software that I remembered from a 8 years ago but it’s actually quite excellent.  Since my previous experience with modeling was with 3D Studio back in school the transition from a mouse-centric environment to the hotkey-centric environment of Blender was quite smooth – even though I had to go and buy a mouse with a middle button. After creating a snake, a blob and a few cubes I finally built a room with an arcade machine. The arcade machine has the exact dimensions of the original Q*Bert arcade cabinet and the room serves as the players home base before literally diving into the game.

###Polish
When everything began to come together I decided to spend some time on the graphics. The first thing I did was to  try and get proper lighting working but I soon realized that learning advanced lighting techniques was not within my reach, so instead of bashing my head against a shader I went for a somewhat cheap approach and added the shadows directly to the texture of my cube. I’ve since then learned that this technique is called lightmapping and that it is actually used in all the pretty games. I’ve also learned that Blender can bake these lightmaps for you, a thing that would have been really good to know earlier. =)

##The bad
From my experience the only bad things are the ones you cannot learn from, but when you are on the tight schedule of a jam everything that wastes time and does not end up in the final product is bad, and boy did I have my share of it!

<img src="/images/softbody-cat.jpg" style="float:right">
**Softbodies** are like cats. They are nice to look at but as soon as you try to get them to do what you want hell breaks loose! I initially wanted to used softbodies for the blob character, and getting softbodies to work in Bullet is  actually not that hard. The tricky part is to make softbodies do any of the following.

 - Change direction – since the blob moves down the pyramid in a random fashion
 - Translate from one point to another – since the blob need to me moved to the top of the pyramid
 - Collide with rigid bodies – since the player has to die
After trying to get softbodies working with the actual game for a few hours I simply decided that they weren’t in the 80′s spirit I was going for and went with a more traditional approach.

**Frogger ending**. It may sound cool, but spending a lot of time in blender modeling a 3D frogger level that would work as the end sequence is no something you should do the day before the jam ends. Needles to say – frogger ending was killed and a less overkill ending was put into its place.

##The ugly
Not realizing that scale * rotate * translate does not take into account that C++ starts with the last parameter. Let’s never talk about this ever again.

##Conclusion
All in all I am very happy with what I accomplished in such a short time. I can’t say I know C++ but I have a fair grasp of the language and I’ve continued to work on other projects using some of the other techniques I used on V^Bert. I’m also quite satisfied how the game turned out. It’s fun, it got a unique jumping mechanic and it does not make me sick – and what more could anyone ask of a VR game? =)
