---
layout:     post
title:      Kangaroo Dash - a retrospective
image:		kangaroo_dash_jam.jpg
date:       2015-06-02 22:31:19
summary:    When Oculus announced the GearVR jam back in February I didn't take much notice. I had read about the device and watched the various presentations on Oculus Connect but it always felt kind of gimmicky, and why would..
categories: oculus_rift
---

When Oculus announced the GearVR jam back in February I didn't take much notice. I had read about the device and watched the various presentations on Oculus Connect but it always felt kind of gimmicky, and why would
anyone use a mobile phone to do limited VR when you could just use a gaming rig and get the full experience?

##Getting into mobile VR
I continued on my usual path until I watched [Carmacks speech](https://www.youtube.com/watch?v=CqdexZJFHQE) at GDC. It really got me thinking about mobile VR and the obvious benefits of being able to have an untethered device that would just be an extension of your
smartphone. This was indeed the way to get virtual reality out to the masses, but my place in the equation was still unclear and the VR jam was still just a lingering thought at the back of my head.

Then I got _the_ email.

It was from Aaron Davies at Oculus asking me if I wanted to take my [2013 jam entry](/oculus_rift/2013/09/11/vbert-a-retrospective/) to the GearVR. My mind went into a spin, someone at 
Oculus actually like my game!

After sending a few emails back and forth we agreed on that I would try to create a V^Bert version for the Gear, or something with a similar mechanic. The reason for not just porting V^Bert to the Gear is the obvious
legal issues surrounding Q^Bert, and while I like do a challenge I did not particularly look forward to creating a game just to have it shut down in the last minute.

##Making a game
Now, saying that you will make a game and actually coming up with an idea and implementing it are two very different things. To ease the pressure of creating a V^Bert successor I decided that entering the VR Jam would be a good
way to learn Unity, brush off my somewhat lacking blender skills and basically just getting to know the hardware until I would develop the _real_ game.

The actual hardware would arrive around the second milestone and there was still two weeks before the jam would start. Being true to the Ludum Dare spirit I decided not to start writing any code or creating any assets until
the jam had officially started. Having no code to write and no models to create I started to play around with some basic ideas. I knew I wanted to keep the jumping since it is currently the only way for me to freely roam the environment
without getting motion sick (it's either that or being in a virtual car). Since I'm a fan of old arcade games I started to search my mind to see if there was any game that would fit the control scheme I had in mind, and I did not have to
search for long until frogger popped up. For those of you that are not nostalgic about these thing just imagine crossy road but with much worse graphics.

With an basic idea of what I wanted to do I waited for the competition to start.

It was a long wait.

##Jam time!
When the competition started I quickly created a basic prototype of a game where the user would jump across an infinite level that contained roads, rivers and trains.
It was awful.
I has basically created a walk-across-the-street-simulator and it was a complete waste of VR. Remember the last time you had fun crossing a street? No? Didn't think so.

After a few hours of panic I decided to start over from scratch. The jumping mechanic worked well, I just had to figure everything else out.

Now, I'd love to give you a detailed story about how I created various design documents, detailed sketches and then went on to a very clean and extendable implementation. But that's not how 
things work. The main idea was to create a world full of traps and other things that the player would have to avoid to reach the goal. The pacing was centered around a look-think-act cycle that was
interrupted by a few "run for your life" - moments. The implementation was mostly based on trial and error because in VR, what feels good on paper might feel awful in VR (just try to lerp at 200kmh in the middle of the night and you'll know what i mean).

###The things I managed to do right
I decided to have an iterative approach and make self contained sections of fun that I would then connect with each other. Having each section self contained meant that I could work on a small part of the whole without losing focus. 
Another benefit is that the game was pretty easy to pace due to the fact that I could just sort the individual sections on difficulty and then join them together in a level.

Another thing that went rather well is creating a game that is _easy to play but hard to master_. Jumping comes natural to people and while conducting playtesting on my coworkers and friends I noticed that out of 35 people only about 10% had any difficulty
understanding how to play the game after getting a simple "just jump" - instruction. Out of the remaining 90% I would estimate that 50% completed the first level and 5 people managed to finish the whole game, which took them between 11 and 20 minutes. People 
doing the longer sessions always found their own particular style of jumping which look weird and awesome at the same time.

###Regrets and a horrible mess
I do not have many regrets and all in all everything went well. The biggest problem I had was with Unity. I early on decided that I wanted to bake everything to keep the framerate up, but switching to Unity 5 before I had gotten my
hands on the actual hardware was a huge mistake. When testing the game on the DK2 everything looked fine, excellent even. When testing it on the Gear textures swapped out randomly and the game felt like a twisted version of hell. To make 
a long story a bit short I ended up having to recreate the game in Unity 4. Going back to an earlier version was a no-go since I had worked for about a few days implementing a lot of the basic functionality in the game. Recreating everything
took about two days and by the end of the day I probably ended up with a cleaner version of the game then I would had done otherwise.

###How to fail
When the day came for the finalists to be announced I was quite optimistic. I had played a lot of the games in the jam and I thought my chance of reaching the finals was good, and the fact that innovation was a judging criteria did not make things worse. 
I got the email early morning and my heart sank a bit when I realized that all hard work had been for nothing.

Not a finalist.

It's very easy to lash out in anger in times like this. The initial judging was done on video and description only which at this time felt extremely unfair. But, I had read the rules and after a slice of excruciating torment things
settled down.

##Moving forward
After dumping a lot of my feelings in a [forum post](https://forums.oculus.com/viewtopic.php?f=77&t=23494) I decided that I liked my game enough to take it to the store. It is in my eyes a better game than V^Bert and I have gotten some great feedback from people 
playing the game. The time wasted would only be truly wasted if a good game did not reach the GearVR store.

So, prepare yourself for the best kangaroo simulator on the GearVR - coming this fall!

<iframe width="560" height="315" src="https://www.youtube.com/embed/tWPbhBGRxxI" frameborder="0" allowfullscreen></iframe>

[Download APK](http://vrjam.challengepost.com/submissions/36759-kangaroo-dash)
