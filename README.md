# AI-generated Artifacts

https://user-images.githubusercontent.com/22293597/231271067-a53819bf-9cb4-49ec-bdf8-b9b1a969ed8e.mp4


## Requirements
* Midjourney, Dall·E 2, or Stable Diffusion.
* Adobe Substance Sampler
* Blender 2.5 or newer

## Limitations
* Can only generate mirrorable objects. Complex objects like chairs are not recommended.


## Tutorial
Going from text to 3d model requires the following steps: (1) Generate image from text, (2) generate simple mesh from generated image, (3) generate height map from image, and (4) apply height map to simple mesh in Blender. The total process roughly takes 10-30 minutes pr. object.

1. Open your favorite text-2-image generator of choice. I personally like to use [Midjourney](https://midjourney.com/) v4. In here, prompt the model to generate an image of with a sideview of the object you want to generate. For this using "Sideview of [object]" usually does the trick. Feel free to add quality words like "design award" at the end to ensure good quality.

<img width="100%" alt="image" src="https://user-images.githubusercontent.com/22293597/231287919-377ada12-0146-4d53-8adf-73a26e261a15.png">

2. Once you have an image that you like, go to [MonsterMash](https://monstermash.zone) and press the the arrow next to the "folder" icon > "import template image" > your generated image from step 1. Once your image is loaded, draw as precisely as possible around the edges of your object in one long line. When done, press the "inflate" button and then the arrow next to the "download" icon > "Export current animation frame as .obj file".

<img width="100%" alt="Skærmbillede 2023-04-11 kl  5 07 38 PM" src="https://user-images.githubusercontent.com/22293597/231288757-b7a595de-de9a-44e8-8989-eaff94d38614.png">

3. Open Substance Sampler 3D and press "Create new". Drag and drop your generated image from step 1 into the program. Choose Image to Material (AI powered). After the process is done, fiddle around with the settings really get the features that you want to be popping. You can play with the displacement height scale in the bottom of the UI. When done, press the "share" button on the right side of the UI and "export as". Once exported you will find the height material in the exported folder.

![vase-textures](https://user-images.githubusercontent.com/22293597/231289704-13f97b0a-fb13-4c14-8683-5630f64c1d16.jpg)

4. Open Blender and create a new project.
