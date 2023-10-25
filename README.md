# DISCOVER: Visual interpretability of image-based classification models 
Official Tensorflow2 implementation of: Visual interpretability of image-based classification models by generative latent space disentanglement applied to in vitro fertilization

## Main requirements
* Python 3.9.10
* tensorflow 2.6.2


## Method Overview
DISCOVER is a designated general-purpose interpretability “discovery machine” especially geared toward quantitative interpretation 
of known and new classification-driving semantic image properties. 
DISCOVER is a generative model that learns representations designed to discover the underlying visual properties driving image-based
classification models. The main innovation of our method is a disentangling module that optimizes a classification-driven and disentangled
latent representation, where a subset of latent features encapsulates the discriminative information of the classification model, 
and where each of these latent features encodes a distinct visual property in the image that is important for classification and that
is distinct from the ones encoded by other latent features.

![architecture](./DOCS/DISCOVER_architecture.png)


## CelebA GENDER analysis
* Open notebook DISCOVER/GENDER/GENDER_ANALYSIS.ipynb.
* Find and change 'data_path = <PATH>' to local path.
* This will automatically load the saved classifier and DISCOVER models
* Run notebook and see the comments in each cell to understand which analysis is taking place.

## Interpreting a new dataset (celebA or other)
# Train classifier:
* Any CNN classifier model can be used. Here the notebook DISCOVER/GENDER/GENDER_CLF_TRAINING.ipynb is given for ease of use.
* Update the TRAIN TEST images folders for classes 0 and 1 in the DISCOVER/GENDER/IMAGES folder.  
* For celebA download data from: https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html. 
* Find and change 'data_path = <PATH>' to local path.
* This will automatically load the saved classifier and DISCOVER models
* Run notebook and see the comments in each cell to understand which analysis is taking place.
* save the trained model to the data_path. (for celebA it is named GENDER_CLF_SAVED_MODEL.h5)

# Train DISCOVER:
* Find and change 'data_path = <PATH>' to local path.
* This will load the data and the saved classifier model (for celebA it is named GENDER_CLF_SAVED_MODEL.h5)
* DISCOVER uses the inner layers of the classifier. Update the names of the inner layers you wish to use. reccomended to use the deeper layers.
Find 'clf_outputs' and update the names from the classifier by running clf_model.summary(). 
* To upload previous saved DISCOVER model switch on upload_saved_model=1. These models are saved in DISCOVER/GENDER/GENDER_DISCOVER_SAVED_MODELS.
# Run notebook. Allow saving of the model network in the final cell.

## Licence
This work is released under the MIT licence.

