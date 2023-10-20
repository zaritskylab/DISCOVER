# DISCOVER: Visual interpretability of image-based classification models 
Official Tensorflow2 implementation of: Visual interpretability of image-based classification models by generative latent space disentanglement applied to in vitro fertilization


![architecture](./DOCS/DISCOVER_architecture.png)


## Requirements
* Python 3.9.10
* tensorflow 2.6.2

## IVF analysis
![IVF analysis](./DOCS/IVF_explanations.png)

## GENDER faces analysis
![GENDER analysis](./DOCS/GENDER_explanations.PNG)

## Training celebA or other custom data
* Download celebA data: https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html and save images in 'IMAGES' folder according to current split (MALE_TRAIN/FEMALE_TRAIN/MALE_TEST/FEMALE_TEST) 
* To train the classifier with celebA data:  use 'GENDER_CLF_TRAINING.ipynb'. Update 'data_path' prefix and run code.
* To train DISCOVER with trained classifier: use 'GENDER_DISCOVER_TRAINING.ipynb'. Update 'data_path' prefix and update 'GENDER_CLF_SAVED_MODEL.h5' saved model. 
* To analyze and interpret results:          use 'GENDER_ANALYSIS.ipynb'. update 'data_path' prefix and GENDER_CLF_SAVED_MODEL.h5 and 'GENDER_DISCOVER_SAVED_MODELS'.

## Licence

This work is released under the MIT licence.

