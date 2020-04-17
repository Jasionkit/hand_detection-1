original web
https://github.com/molyswu/hand_detection

using Neural Networks (SSD) on Tensorflow.

This repo documents steps and scripts used to train a hand detector using Tensorflow (Object Detection API). As with any DNN based task, the most expensive (and riskiest) part of the process has to do with finding or creating the right (annotated) dataset. I was interested mainly in detecting hands on a table (egocentric view point). I experimented first with the [Oxford Hands Dataset](http://www.robots.ox.ac.uk/~vgg/data/hands/) (the results were not good). I then tried the [Egohands Dataset](http://vision.soic.indiana.edu/projects/egohands/) which was a much better fit to my requirements.

The goal of this repo/post is to demonstrate how neural networks can be applied to the (hard) problem of tracking hands (egocentric and other views). Better still, provide code that can be adapted to other uses cases.

If you use this tutorial or models in your research or project, please cite [this](#citing-this-tutorial).

Here is the detector in action.

<img src="images/hand1.gif" width="33.3%"><img src="images/hand2.gif" width="33.3%"><img src="images/hand3.gif" width="33.3%">
Realtime detection on video stream from a webcam .

<img src="images/chess1.gif" width="33.3%"><img src="images/chess2.gif" width="33.3%"><img src="images/chess3.gif" width="33.3%">
Detection on a Youtube video.

Both examples above were run on a macbook pro **CPU** (i7, 2.5GHz, 16GB). Some fps numbers are:


| FPS  | Image Size | Device| Comments|
| ------------- | ------------- | ------------- | ------------- |
| 21  | 320 * 240  | Macbook pro (i7, 2.5GHz, 16GB) | Run without visualizing results|
| 16  | 320 * 240  | Macbook pro (i7, 2.5GHz, 16GB) | Run while visualizing results (image above) |
| 11  | 640 * 480  | Macbook pro (i7, 2.5GHz, 16GB) | Run while visualizing results (image above) |

> Note: The code in this repo is written and tested with Tensorflow `1.4.0-rc0`. Using a different version may result in [some errors](https://github.com/tensorflow/models/issues/1581).
You may need to [generate your own frozen model](https://pythonprogramming.net/testing-custom-object-detector-tensorflow-object-detection-api-tutorial/?completed=/training-custom-objects-tensorflow-object-detection-api-tutorial/) graph using the [model checkpoints](model-checkpoint) in the repo to fit your TF version.



**Content of this document**
- Motivation - Why Track/Detect hands with Neural Networks
- Data preparation and network training in Tensorflow (Dataset, Import, Training)
- Training the hand detection Model
- Using the Detector to Detect/Track hands
- Thoughts on Optimizations.

> P.S if you are using or have used the models provided here, feel free to reach out on twitter ([@vykthur](https://twitter.com/vykthur)) and share your work!


## Acknowledgements

This work also served as an intense weekend crash course for me to learn Python and Tensorflow. It would be impossible without the Egohands Dataset, many thanks to the authors! The tensorflow custom object detection guides by [Harrison from pythonprogramming](https://pythonprogramming.net/training-custom-objects-tensorflow-object-detection-api-tutorial/) and [Dat Tran](https://towardsdatascience.com/how-to-train-your-own-object-detector-with-tensorflows-object-detector-api-bec72ecfe1d9) were immensely helpful to this learning process. And ofcourse, many thanks to the Tensorflow authors! Its a great frameworks!




If you have created something cool, send me a note (or tweet) and I'll be happy to include it here!

## Citing this tutorial

If you'd like to cite this work, use the below.

Victor Dibia, Real-time Hand-Detection using Neural Networks (SSD) on Tensorflow, (2017), GitHub repository, https://github.com/victordibia/handtracking
```bib
