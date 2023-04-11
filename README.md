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

2. Once you have an image that you like, go to [MonsterMash](https://monstermash.zone) and press the the arrow next to the "folder" icon > "import template image" > your generated image from step 1. Once your image is loaded, draw as precisely as possible around the edges of your object in one long line. When done, press the arrow next to the "download" icon > "Export current animation frame as .obj file".

3. Open Substance Sampler 3D and create a new project. Drag and drop your generated image from step 1 into the program. Choose AI powered.

4. Open Blender and create a new project.
