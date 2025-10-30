# ARKit Extra Pendulum Setup
These are a list of additional blendshapes to create for your model to add organic feedback effects to your facetracking. We will create pendulum chains driven by different ARKit tracking blendshapes. You will need to create both positive and negative blendshapes for each of these (ie movement up and movement down)

*(This guide is also published [here](https://publish.obsidian.md/lunazera/Publish+Site/Guides/ARKit+Extra+Pendulum+Setup))*

I'll provide the lists of blendshapes here and reference images for what these should look like. I'll also have all the VNyan pendulum chains I use to drive these here (note some might have extra things on it for my own setup): https://git.gay/lunazera/LZ-VNyan-Library/src/branch/main/Guides/ExtraARKit/chains

To set this up, we need to create new shapekeys on our mesh for all of these rather than using the existing ARKit shapekeys because we can't use those for our tracking and pendulum chains at the same time. We will also need to create left/right versions for many of these if the ARKit blendshape is Left/Right specific.

# Lists of Extra Blendshapes
There's quite a bit here just because we have to create both left & right sides for many of them. I'll split them into groups for the mouth, eyes & brows, and iris & highlights.

You can use my blender [Generate mesh shape keys tool](https://git.gay/lunazera/Blender-Generate-Shapekeys) to quickly add these lists as blank blendshapes on your face mesh *(once that update is finished for it)*

## Mouth
```
move_mouthLeft, move_mouthRight, move_mouthDown, move_mouthUp, stretch_mouthWideLeft, stretch_mouthNarrowLeft, stretch_mouthWideRight, stretch_mouthNarrowRight, stretch_mouthScale, stretch_lipsNeg
```
## Eyes & Brows
```
stretch_eyeWideLeft, stretch_eyeNarrowLeft, stretch_eyeWideRight, stretch_eyeNarrowRight, move_browUpLeft, move_browDownLeft, move_browUpRight, move_browDownRight, move_noseUp, move_noseDown, move_eyelashTipUpLeft, move_eyelashTipDownLeft, move_eyelashTipUpRight, move_eyelashTipDownRight
```
## Iris & Highlights
```
stretch_irisTallLeft, stretch_irisShortLeft, stretch_irisTallRight, stretch_irisShortRight, stretch_irisWideLeft, stretch_irisNarrowLeft, stretch_irisWideRight, stretch_irisNarrowRight, stretch_highlightBigLeft, stretch_highlightSmallLeft, stretch_highlightBigRight, stretch_highlightSmallRight
```

Let me explain some of the thinking/rational for all of this, and then go over references for what these look like.

# ARKit Blendshapes and the movement we want to create from them
- ## eyeBlinkLeft/Right
	- ### iris stretching 
	  `Tall-Short (vertical stretch)` & `Wide-Narrow (horizontal stretch)`
		- Creates Iris wobble effect
	- ### eyelash movement
	  `Tip Up-Down (vertical movement/stretch)`
		- Makes stylized thick eyelashes wiggle a bit
- ## jawOpen
	- ### Mouth scale
	  `mouth/lips Big-Small (stretch/scale)`
		- Creates slight mouth scaling movement when you open or close mouth, giving slight elastic look
- ## eyeWideLeft/Right
	- ### eye stretching
	  `Wide-Narrow (stretch up/down)`
		- Creates wiggle effect when you make your eyes wider
- ## browOuterUpLeft/Right
	- ### brow movement
	  `Move Up-Down (vertical movement)`
		  - Moves eyebrows up and down when raising or lowering brows
- ## mouthSmileLeft/Right
	- ### Mouth stretching
	  `Mouth corner Out-In (stretch horizontal)`
		- Stretches corner of mouth out/in with smiling
	- ### Cheek Wiggle
	  `Cheek Out-In (horizontal`
		- Move cheek out a bit when smiling wide
- ## noseSneerLeft/Right
	- ### Nose Movement
	  `Nose Up-Down (vertical movement)`
		- Moves nose up when you sneer
- ## jawOpen
	- ### Mouth Movement
	  `Mouth Up-Down (vertical movement)`
		- Moves mouth down when you open your mouth
- ## mouthLeft/Right
	- ### Mouth Movement
	  `Mouth Left-Right (horizontal movement)`
		- Wiggles mouth out left/right as you move your mouth
