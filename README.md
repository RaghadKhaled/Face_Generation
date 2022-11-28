# Generate Fake Faces Using GAN

--- 

## Overview

The aim of this project is to create a model capable of generating realistic human images that do not exist in reality. The technology behind these kinds of DL model is called a GAN, or Generative Adversarial Network. 
GANs algorithmic architectures use two networks that work in adversarial manner to create the desired result. The Generator’s goal is to create realistic fake images, while the Discriminator’s goal 
is to distinguish between real images and fake images in order to guide the Generator to create more realistic images. 
I did this project as a part of Deep Learning Nanodegree from Udacity.

--- 

## Dataset

The dataset used in this project is the Large-scale CelebFaces Attributes (CelebA) Dataset. It consists of colored images of human faces and their annotations. Since we use generative networks, we do not need to the annotations. 
You can find more information for the full dataset [on this link]( http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html).

--- 


## Project Steps

The high-level steps of the project include:
1.	Build a CNN to Classify Landmarks (from Scratch) 
2.	Build a CNN to Classify Landmarks (using Transfer Learning)  – I used VGG16 since my dataset has similar feature of the dataset that trained on the VGG16. Therefore, most or all of the pre-trained neural network layers already contain relevant information about the my dataset. I Use all but the last fully connected layer as a fixed feature extractor and I define a new, final classification layer to match the number of classes of my task. I randomize the weights of the new fully connected layer and freeze all the weights from the pre-trained network then I train the network to update the weights of the new fully connected layer.
3.	Create Landmark Prediction Algorithm – this algorithm take the best model I created to make interface for any user-supplied image as input and suggest the top k most relevant landmarks from 50 possible landmarks from across the world. 
All the implementation details are in jupyter notebook file ``` landmark.ipynb```.


---

## Requirements	
- Python 3.7
- Numpy 
- Torch
- Torchvision
- Pickle
- Matplotlib 
- Jupyter Notebook
- Maybe needs to use GPU


---

## Running the project
The whole project is located in the jupyter notebook file ``` dlnd_face_generation ```, you can use the Anaconda environment to open the Jupyter Notebook and install the requirement.
