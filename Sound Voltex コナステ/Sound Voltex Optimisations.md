The following guide will show you how to optimise your PC to reduce stutter and latency in Sound Voltex コナステ

Table of Contents
_____________________
* [The settings to be using on Sound Voltex](#the-settings-to-be-using-on-sound-voltex) - DO THIS BEFORE DOING ANYTHING ELSE 
* [NVIDIA Control Panel Optimisations](#nvidia-control-panel-optimisations) 
* AMD Control Panel Optimisations (WIP)
* [For portrait mode users or users playing the game on a 2nd monitor that are using NVIDIA or pre-RDNA AMD cards](#for-portrait-mode-users-or-users-playing-the-game-on-a-2nd-monitor-that-are-using-nvidia-or-pre-rdna-amd-cards)

# The settings to be using on Sound Voltex 
Copy the following settings on your Sound Voltex settings window before you follow anything else on this guide.
![image](https://user-images.githubusercontent.com/16516667/216709579-e852b674-b0f8-459e-a929-765a7e92e2f6.png)


# NVIDIA Control Panel Optimisations 
Open the NVIDIA Control Panel, head to Manage 3D settings then program settings and press add
![image](https://user-images.githubusercontent.com/16516667/216704603-172b3326-8aa6-47a4-a3ab-14636d6cb403.png)

Press browse and add sv6c.exe to the programs
![image](https://user-images.githubusercontent.com/16516667/216705003-1eed657b-b3a5-4572-8ab1-28ab8affbcc6.png)

Change the following settings for sv6c.exe to match with what I have below.

![image](https://user-images.githubusercontent.com/16516667/216705211-0d72245e-77e4-43b3-90ce-52533b455787.png)

![image](https://user-images.githubusercontent.com/16516667/216705241-c0cf8c0a-7815-46b7-9227-ddd7cd4cc89b.png)

![image](https://user-images.githubusercontent.com/16516667/216705335-088333cf-51a5-4327-8066-35ca8033eec3.png)

![image](https://user-images.githubusercontent.com/16516667/216705371-e14ec08e-8e7c-457c-9fc6-3c4ec534a62e.png)

Why didn't I enable Low Latency Mode on the control panel for Sound Voltex? It's a D3D9 Game, so that option will do NOTHING for this game.


# AMD Control Panel Optimisations 

WIP, I do not have an AMD card, but if you have an AMD card, preferably an RDNA card please hit me up.


# For portrait mode users or users playing the game on a 2nd monitor that are using NVIDIA or pre-RDNA AMD cards

Find your sv6c.exe, right click it, press properties. On the properties window click on the compatiblity tab and press "Disable full-screen optimisations"
![image](https://user-images.githubusercontent.com/16516667/216706432-e833acaa-fc13-41d5-83d4-21f2142afd22.png)

What this does is let you run your game in Legacy Flip giving your game exclusive control of the monitor it is on because NVIDIA and older AMD cards do not support Independent Flip on portrait resolutions or 2nd monitors and will make the game run on Composed Flip. I am not sure if this is a problem on newer AMD cards when playing the game as disabling fullscreen optimisations will not even let you load the game on RDNA AMD cards but from what the current knowledge I have, the newer AMD cards should allow Independent Flip on portrait resolutions. If you have an RDNA AMD card and want to help me test, let me know!

If you want more information how flip model works you can view this [diagram](https://wiki.special-k.info/Presentation_Model#bitblt-d3d11)


NOTE: Enabling this option will not allow you to take screenshots with print screen anymore. It's up to you whether you want to sacrafice latency for being able to use that button.........alternatively you can take out your phone and take scores pics as if you were at the arcade.
IF you really want to  have this option enabled but still be able to take screenshots from your PC you can use OBS to project the game window to it's own window and screenshot that projected window instead. 





