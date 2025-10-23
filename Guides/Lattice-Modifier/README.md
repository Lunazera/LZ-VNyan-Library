# Using the Lattice Modifier in VNyan
*for blink squishes or whatever else you want!*
Related VNyan Discord Thread: https://discord.com/channels/714814460010823690/1385111608765710427

With the move to Unity 2022, we can now use the Lattice Modifier on our models! You can use this for some really cool and interesting things, but I wanted to show how you can make a head squish effect when you blink as an example.

You'll need to purchase the Lattice Modifier from the Unity Asset store to use this. You can get it [here](https://assetstore.unity.com/packages/tools/animation/lattice-modifier-for-unity-293850)
### Things You'll Need
- Unity 2022.3.61f1
- latest VNyan SDK 
- UniVRM 0.104
- Lattice Modifier ([here's the documentation for it](<https://harryheath.com/lattice#skinned-lattice-modifier>))

I made a video tutorial for this :3 also attached is the pendulum chain referenced in the video.

## Quick Tutorial
- Add a new GameObject to your mode, and add the Lattice component to it
- Change the position and scale to fit your head
- Drag the Lattice object to be under your Head bone
- Add Lattice `Skinned Modifier` components to all the meshes on your model you want to be deformed
- Drag the Lattice object into each component
- Make a new Animator component on the Lattice object.
- This this selected, use the Animation window to create a new animation. This should have the top of the lattice move down at the 1:00 time mark.
- Find the `.anim` you made in the project window and make it not loop
- In the Animator window, create a new float parameter called "headsquish"
- under the Layers section, select the animation, click the parameter checkmark next to Motion Time
- With the Lattice object selected again, add a `VNyan Anim Param Link` component. Set the parameter name and Animator parameter name to be "headsquish", and drag in the Lattice object so that the animator points to it.
- Add the pendulum chain file to see an example of controlling this animation with your eyeblinks!

## Video Tutorial
[![](Lattice_Modifiers_Tutorial.mp4)]