# cGAN-colorization-NN-project                                                                               
  

Original paper https://arxiv.org/abs/1611.07004. NNs univeristy project. Have a look to *report.pdf* for explanations.

## Table of contents

* [1 Content description](#1-Content-description)
* [2 Links for models](#2-Links-for-models)

## 1 Content description

### 1.1 Notebooks

You find these files in the "notebooks" directory

* COCO_animals_dataset.ipynb: notebook used for creating the .txt files for the datasets

* cGAN_colorization_training.ipynb: notebook used for cGAN training

* WGAN_colorization_training.ipynb: notebook used for WGAN training

* Classifiers_evaluation.ipynb: notebook used for trainining the classifier C_c

* Evaluation_Metrics.ipynb: notebook used for evaluating generators (and plots)



### 1.2 Files used in order to create the datasets

You find these files in the directory "datasets"

* data_big_training.txt and data_small_training.txt: read the training notebooks and use them

* test_animals.txt


### 1.3 Losses

In "losses" you find the .csv files with the losses obtained during the several trainings


## 2 Links for models

### 2.1 Generators

* WGAN: https://drive.google.com/file/d/1-56COshEqj9U4ld9sHfW0saI1nFBzSDt/view?usp=share_link
* cGAN m=8, N=9.6K: https://drive.google.com/file/d/1--exxKfax4IRfiZg2NB3r9sNB2wUl-JU/view?usp=share_link
* cGAN m=32, N= 9.6K: https://drive.google.com/file/d/1mZe-9ZUE7P0n_KqQnzXxk6DZFYDrjtVC/view?usp=share_link
* cGAN m = 32, N=16K: https://drive.google.com/file/d/1--Ff6eXKU81SMNBtS5FXeLV6NMtWOTpC/view?usp=share_link

### 2.2 Classifiers:
* vgg16 (used for the metric 1 and 2): https://drive.google.com/file/d/1vl9i0lGVEW7f0Y-sWJLOgmMpG56_Tled/view?usp=share_link

* vgg16 (used for the metric 3): https://drive.google.com/file/d/1-JlZdvmMEJEHlWvZvYX118M_eWzPIdd0/view?usp=share_link

#### Here we have all the pretrained classifiers for the metric 3 (weight comparison)

* WGAN: https://drive.google.com/file/d/1-G2-FKH9dONevdm7sFLragB90piZUMWG/view?usp=share_link
* cGAN m=8, N=9.6K: https://drive.google.com/file/d/1-ix-DU7bgK8rkGb-3frb7QOrtXJ2STYb/view?usp=share_link
* cGAN m=32, N= 9.6K: https://drive.google.com/file/d/1-W-gekJpuU_z6rn4tJKRolxv5AMui04b/view?usp=share_link
* cGAN m = 32, N=16K: https://drive.google.com/file/d/1-Dn_aMjyVmNEEXGN9amandL0jSSMDFrV/view?usp=share_link

## Results (visual example)

Real images:
![real](https://user-images.githubusercontent.com/83876494/218174501-44801234-e4f9-4d83-b2db-8048f4eb2cbc.jpeg)

Fake images (obtained with cGAN m=32, N = 9.6K):
![fake](https://user-images.githubusercontent.com/83876494/218174776-6d97c024-31fc-4a09-8b9a-b52a5b9acad1.jpeg)
