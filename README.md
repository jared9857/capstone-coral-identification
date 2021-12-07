# Coral Identification
![image](https://user-images.githubusercontent.com/82346896/144655954-1b581ac6-36bd-42ba-930f-f77d527d2adb.png)
## Overview

Unfortunately all around the world coral reefs are dying out. Due to climate change, ocean temperatures are slowly rising causing the event of coral bleaching. While pure white bleached coral may carry a beauty of its own, bleached coral is a very bad thing. Coral bleaching occurs when ocean temperatures increase. Even one or two degrees Farenheit can cause coral bleaching. Coral can recover from bleaching, but as ocean temperatures keep rising more coral is getting killed by bleaching each year. In order to better track this disaster, I built a Convolutional Neural Network that can classify between living, bleached, and dead coral.

## Business Problem
![image](https://user-images.githubusercontent.com/82346896/144662657-66a63520-7e46-437b-afb1-402d2cdbe6a1.png)

I have always had a deep love for the ocean, so when I got the idea for this project I was energized. I really wanted to find a way that I could use Machine Learning to help heal the oceans. I ended up coming across the organization The Great Reef Census. The Great Reef Census is a community driven organization that's goal is to survey the various parts of the Great Barrier Reef. The Great Barrier Reef is very large and surveying it is a very large task. So they have volunteers who have participated in surveys take photos and some basic data on the area of the reef they went to. I highly recommend checking out their [website](https://greatreefcensus.org) if you would like to learn more or explore some of the user submitted surveys. In order to get more detailed information I thought it could be useful to build a classification model that could identify between dead, living, and bleached coral. This way, the model could be used to track the genral health of the reef by tracking the percentage of dead, living, and bleached coral in each area based on the models identifications.

## Data

The data set I used to build and train my model was a public data set from [Kaggle](https://www.kaggle.com/sonainjamil/bhd-corals) that contained 1582 labeled images of living, dead, and bleached coral. I used these images to train my model on, but I made sure to pull random images from each class to build our testing set that the model was never trained on. 
## Methods

![image](https://user-images.githubusercontent.com/82346896/144683954-62a8087d-5c4c-43b3-a5ec-fa18f6352d5c.png)
The final model I used was a Convolutional Neural Network. I built this model by starting with a very basic and bare Neural Network and then adding layers, tweaking settings, and multiple test runs. In order to help deal with our small data set, I implemented a large amount of image augmentation. Over each epoch the Neural Network goes through, the model will apply one of methods of augmentation to the photo. It might flip it one way, rotate it X amount of degrees, or zoom in a random amount within a range I set. This effectively increases the number of images we can train on. Image augmentation was key in getting my models accuracy up.

### Results

The final CNN model had an Accuracy score of 92%.

### Possible Shortcomings
#### - Class Imbalances
The data I used contains some large class imbalances. The data has around six times as many photos of living and bleached coral when compared to the images of our dead coral. Having similar numbers of each image type would help improve our model.

#### - Small Dataset
The dataset I used only had 1,500 images. This would likely reduce our models effectiveness in the field because our model has only seen a very limited set of images. It would only benefit the model to increase the amount and variety of the images used to train and build the model with.

#### - Lack of Field Accurate Photos
The images I used to build this model are not from the Great Reef Census. In order to more effectively deploy this model it would make the most sense to train the neural network on user submitted images. Survey photos could be taken at all sorts of angles, in a variety of lighting, and with varying image quality. Training the network on these images would help improve the models in field performance.

## Conclusions

In the end I built a CNN model and trained it on images of living, bleached, and dead coral. The model's final accuracy was 92% when classifying my test data. 
## For More Information
For more information, please take a look at my [Jupyter Notebook](https://github.com/jared9857/capstone-coral-identification/blob/main/Final_Notebook.ipynb) or view my presentation [here](https://docs.google.com/presentation/d/1rVIYAAEjp_cCWFrBVkbMVZ-ao1IbtQNFVID03p0tCKw/edit?usp=sharing).
## Repository Structure
