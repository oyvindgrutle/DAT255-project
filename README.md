# DAT255-project

## Table of contents

| Notebooks    |
|:----------|
|  [0-Downloading-and-Exploration.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/0-Downloading-and-Exploration.ipynb)  |
|  [1-Free-Sound-Classifier.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/1-Free-Sound-Classifier.ipynb)  |
|  [2-Transfer-Learning-Data-Collection.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/2-Transfer-Learning-Data-Collection.ipynb)  |
|  [3-Transfer-Learning-Urban-Sound-Classifier.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/3-Transfer-Learning-Urban-Sound-Classifier.ipynb)  |
|  [4-Free-Sound-Classifier-App.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/Application.ipynb)  |

---

## Introduction

This repository contians multiple notebooks exploring the dataset from the Freesound General-Purpose Audio Tagging Challenge, which is available to download on Kaggle: https://www.kaggle.com/c/freesound-audio-tagging/overview

What we have created is a model for classifying the different aduio files from the dataset into the 41 different categories. After exporting this model we experimentet with transfer learning and using our own pretrained model on a new dataset. For this we used the UrbanSound Dataset. More info on this dataset and download can be found on this site: https://urbansounddataset.weebly.com/urbansound.html

Our methods are mostly built on the fastai library and the methods used in the [fastai course](https://course.fast.ai/).

[Librosa](https://librosa.org/doc/latest/index.html) is also used a lot to process and manage the audiofiles and make image representations of the audio files in order to classify them as images.

## Motivation

Machine learning with audio can be used in many different situations. From simple usage like creating an application for predicting bird sounds to more complex task like audio transcription.
The model we have created might not have a direct purpose in solving a problem. However it does give a good indication on what is possible with audioclassification. We have also used our model for transfer learning which gave a better result than starting with the resnet34 from fastai. A lot of the labels in the dataset where everyday sounds and a lot of human produced noises like laughing, burping or farting. Since the model now recognized these sounds it could potentially be helpful when training a model to transcirbe spoken sentences or words where there might be background noise or other noises present.

---
