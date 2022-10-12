# neural-networks-project-gesture-recognition-upgrad

## Members in the group:
- Vinay singh shekhawat
- Suraj BS

## Problem Statement

Imagine you are working as a data scientist at a home electronics company which manufactures state of the art __smart televisions.__ You want to develop a cool feature in the smart-TV that can __recognise five different gestures__ performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:
- Thumbs up: Increase the volume
- Thumbs down: Decrease the volume
- Left swipe: 'Jump' backwards 10 seconds
- Right swipe: 'Jump' forward 10 seconds
- Stop: Pause the movie

## Understanding the Dataset

The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a __sequence of 30 frames(images).__ These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

The data is in a zip file. The zip file contains a 'train' and a 'val' folder with two CSV files for the two folders. These folders are in turn divided into subfolders where each subfolder represents a video of a particular gesture. Each subfolder, i.e. a video, contains 30 frames (or images). Note that all images in a particular video subfolder have the same dimensions but different videos may have different dimensions. Specifically, videos have two types of dimensions - either 360x360 or 120x160 (depending on the webcam used to record the videos). Hence, you will need to do some pre-processing to standardise the videos.

Each row of the CSV file represents one video and contains three main pieces of information - the name of the subfolder contiaining the 30 images of the video, the name of the gesture and numeric label (between 0-4) of the video.

Your task is to train a model on the 'train' folder which performs well on the 'val' folder as well.

## Goals of the project:
1. __Generator:__ The generator should be able to take a batch of videos as input without any error. Setps like cropping, resizing and normalization should be performed successfully.
2. __Model:__ Develop a model that is able to train without any errors which will be judged on the total number of parameters (as the inference(prediction) time should be less) and the accuracy achieved.
3. __Write up:__ This should contain the detailed procedure followed in choosing the final model. The write up should start with the reason for choosing the base model, then highlight the reasons and metrics taken into consideration to modify and experiment to arrive at the final model.