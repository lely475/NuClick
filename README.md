# Adapted NuClick for generating ground truth for the OCELOT 2023 Challenge
This repository provides the NuClick code ([link to original repo](https://github.com/navidstuv/NuClick)) as adapted for generating segmentation ground truth maps for the [OCELOT 2023 Challenge](https://ocelot2023.grand-challenge.org/).

## Idea
 NuClick enables nuclei segmentation with the help of a guiding signal. 
 In our case the guiding signal is the cell centroid coordinate, which is given as the cell ground truth for the OCELOT train data. This way we obtain ground truth segmentation maps for the OCELOT 2023 Challenge by using NuClick ([link to NuClick paper ](https://arxiv.org/abs/2005.14511) ).
 
![alt text](gifs/11.gif "H&E")![alt text](gifs/22.gif "H&E") ![alt text](gifs/33.gif "H&E")

## Requirements

`Keras==2.2.4
h5py
opencv-python-headless==4.1.2.30
pandas==0.25.1
matplotlib==3.1.1
six
tensorflow-gpu==2.4.0
scipy
numpy
albumentations==0.3.1
scikit-image
Pillow==8.0.1
`

 ## Inference:
 Download weights for nucleus segmentation from [here]( https://drive.google.com/open?id=1MGjZs_-2Xo1W9NZqbq_5XLP-VbIo-ltA) and save it inside `weights` folder:
 * Define directories in the `config.py`:  `mat_path = ''` ,  `images_path = ''` and `save_path = ''`
 * run `test_all_images`
 
