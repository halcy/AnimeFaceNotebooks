# AnimeFaceNotebooks
Notebooks and some data for playing with animeface stylegan2 and deepdanbooru. Versions for colab included (colab/ directory, or links below)

## Stylegan2 Anime Face model
This notebook has a few simple functions to use stylegan2s projection code to project input images (quality of results varies, but honestly surprisingly good), and sliders for interactively modifying a few tags. The directions in dlatent space were obtained by generating a lot of faces, tagging them with deepdanbooru, and then finding a regression line in disentangled latent space fit to the tag confidence values from deepdanbooru. This version uses Lasso regression to try and exploit sparsity in the disentangled latent space. There's some development notes in the notebook, and code that you can use to calculate your own directions. latents/dlatents + tags for 100000 generated images are included.

<a href="https://colab.research.google.com/github/halcy/AnimeFaceNotebooks/blob/master/colab/Stylegan2_Playground.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Example Video: http://www.youtube.com/watch?v=GRG6czAZql0

[![Stylegan2 Anime Face Interactive Modification](https://img.youtube.com/vi/GRG6czAZql0/0.jpg)](http://www.youtube.com/watch?v=GRG6czAZql0)

## Deepdanbooru + GradCam
This notebook as functions for using DeepDanbooru for tagging, for calculating gradcam maps and post-processing them into activation maps for specific tags, and for then visualizing these maps.

<a href="https://colab.research.google.com/github/halcy/AnimeFaceNotebooks/blob/master/colab/DeepDanbooru-Playground.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Screenshot:

![Shaw (arknights) with tail highlited using gradcam](https://raw.githubusercontent.com/halcy/AnimeFaceNotebooks/master/example_data/gradcam_tagmaps.png)
