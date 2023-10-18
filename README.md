# DISCOVER: Visual interpretability of image-based classification models 
Official Tensorflow2 implementation of: Visual interpretability of image-based classification models by generative latent space disentanglement applied to in vitro fertilization


![architecture](./DOCS/DISCOVER_architecture.png)


## Requirements
Python 3.9.10
tensorflow 2.6.2

## IVF analysis
![IVF analysis](./DOCS/IVF_explanations.png)

## GENDER faces analysis
![GENDER analysis](./DOCS/GENDER_explanations.PNG)

## Training
* To train the classifier with custom data: update 'data_path' and split data to train/test in the 'IMAGES' folder.
* To train DISCOVER with trained classifier: update 'data_path' and 'IMAGES' folder. update classifier.h5 saved model. 
* To analyze and interpret results: update 'data_path' and 'IMAGES' folder. update 'CLF_SAVED_MODEL.h5' saved model. update 'DISCOVER_SAVED_MODELS' folder.  

## Licence

This work is released under the MIT licence.

