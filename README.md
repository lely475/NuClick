# Adapted NuClick for generating ground truth for the OCELOT 2023 Challenge
This repository provides the NuClick code ([link to original repo](https://github.com/navidstuv/NuClick)) as adapted for generating segmentation ground truth maps for the [OCELOT 2023 Challenge](https://ocelot2023.grand-challenge.org/).

## Idea
 NuClick enables nuclei segmentation with the help of a guiding signal. 
 In our case the guiding signal is the cell point annotation from the OCELOT train data. This way we obtain ground truth segmentation maps for the OCELOT 2023 Challenge by using NuClick ([link to NuClick paper ](https://arxiv.org/abs/2005.14511) ).


Original image | Cell point annotations<br>(OCELOT ground truth) | NuClick prediction
-------------------------|-------------------------|-------------------------
![alt text](https://github.com/lely475/NuClick/assets/62755943/f2851434-3070-4629-b1cf-2b952f17c1a1) |  ![alt text](https://github.com/lely475/NuClick/assets/62755943/29f7d2e5-b23f-490d-ac26-82f93def9f20) | ![alt text](https://github.com/lely475/NuClick/assets/62755943/04eb2a56-0a29-405d-be1f-b8a2de4452a1)

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
 
## Credits
```
@article{DBLP:journals/corr/abs-2005-14511,
  author       = {Navid Alemi Koohbanani and
                  Mostafa Jahanifar and
                  Neda Zamani Tajadin and
                  Nasir M. Rajpoot},
  title        = {NuClick: {A} Deep Learning Framework for Interactive Segmentation
                  of Microscopy Images},
  journal      = {CoRR},
  volume       = {abs/2005.14511},
  year         = {2020},
  url          = {https://arxiv.org/abs/2005.14511},
  eprinttype    = {arXiv},
  eprint       = {2005.14511},
  timestamp    = {Wed, 03 Jun 2020 11:36:54 +0200},
  biburl       = {https://dblp.org/rec/journals/corr/abs-2005-14511.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
}
```
