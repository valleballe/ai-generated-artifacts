# AI-generated Artifacts

<p align="center">
<video src="https://user-images.githubusercontent.com/22293597/231271067-a53819bf-9cb4-49ec-bdf8-b9b1a969ed8e.mp4" width="300px" autoplay/>
</p>


## Requirements
- [`Midjourney`](https://midjourney.com), [`Dall·E 2`](https://labs.openai.com), or [`Stable Diffusion`](https://stability.ai/blog/stable-diffusion-public-release)
- [`Adobe Substance Sampler`](https://www.adobe.com/products/substance3d-sampler.html)
- [`Blender 3.4`](https://www.blender.org/download/) or newer

## Limitations
* Can only generate mirrorable objects. Complex objects like chairs are not recommended.


## Tutorial
Going from text to 3d model requires the following steps: (1) Generate image from text, (2) generate simple mesh from generated image, (3) generate height map from image, and (4) apply height map to simple mesh in Blender. The total process roughly takes 10-30 minutes pr. object.

1. Open your favorite text-2-image generator of choice. I personally like to use [Midjourney](https://midjourney.com/) v4. In here, prompt the model to generate an image of with a sideview of the object you want to generate. For this using "Sideview of [object]" usually does the trick. Feel free to add quality words like "design award" at the end to ensure good quality.

<img width="100%" alt="Midjourney Outputs" src="https://user-images.githubusercontent.com/22293597/231287919-377ada12-0146-4d53-8adf-73a26e261a15.png">

2. Once you have an image that you like, go to [MonsterMash](https://monstermash.zone) and press the the arrow next to the "folder" icon > "import template image" > your generated image from step 1. Once your image is loaded, draw as precisely as possible around the edges of your object in one long line. When done, press the "inflate" button and then the arrow next to the "download" icon > "Export current animation frame as .obj file".

<img width="100%" alt="MonsterMash" src="https://user-images.githubusercontent.com/22293597/231288757-b7a595de-de9a-44e8-8989-eaff94d38614.png">

3. Open Substance Sampler 3D and press "Create new". Drag and drop your generated image from step 1 into the program. Choose Image to Material (AI powered). After the process is done, fiddle around with the settings really get the features that you want to be popping. You can play with the displacement height scale in the bottom of the UI. When done, press the "share" button on the right side of the UI and "export as". Once exported you will find the height material in the exported folder.

<img width="width=100%" alt="Substance sampler" src="https://user-images.githubusercontent.com/22293597/231334186-c04004a9-d39b-4608-88de-8652353611c7.png">


4. Open Blender and create a new project. Then go to "file" > "import" > "Wavefront (obj)" and import your mesh from step 2. Next, select the imported object and go to the blue wrench icon on the right. Here, press "Add Modifier" and select "Subdivision Surface". Add another modifier called "Displace". When both modifiers are added, it is important that the displace modifier is beneith the subdivision surface modifier. Next, change the "Coordinates" setting from "Local" to "UV" and the "Direction" to "Normal". Finally, adjust the strength to a level that you are satisfied with. Polish the model as desired --- and you're done! I hope this repository was helpful. Please, make sure to cite it or send me an email if you end up using it in any project! I would love to see what you make.

<img width="width=100%" alt="Blender" src="https://user-images.githubusercontent.com/22293597/231333834-58cc521f-2b42-4a55-80d8-bddec097f66f.png">

##  Contribute

AI Generated Artifacts is under active development and contributors are welcome. If you have any suggestions, feature requests, or bug reports, please open new [issues](https://github.com/valleballe/ai-generated-artifacts/issues) on GitHub. 

## BibTeX Citation

If you use AI Generated Artifacts in a scientific publication or installation, we would appreciate using the following citations:

```
@software{danry2023,
  author = {Danry, Valdemar},
  month = {4},
  title = {{AI-Generated Artifacts}},
  url = {https://github.com/valleballe/ai-generated-artifacts},
  year = {2023}
}
```
