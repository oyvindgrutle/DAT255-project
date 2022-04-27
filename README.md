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

## Description

This repository contians multiple notebooks exploring the dataset from the Freesound General-Purpose Audio Tagging Challenge, which is available to download on Kaggle: https://www.kaggle.com/c/freesound-audio-tagging/overview

What we have created is a model for classifying the different aduio files from the dataset into the 41 different categories. After exporting this model we experimentet with transfer learning and using our own pretrained model on a new dataset. For this we used the UrbanSound Dataset. More info on this dataset and download can be found on this site: https://urbansounddataset.weebly.com/urbansound.html

Our methods are mostly built on the fastai library and the methods used in the [fastai course](https://course.fast.ai/).

[Librosa](https://librosa.org/doc/latest/index.html) is also used a lot to process and manage the audiofiles and make image representations of the audio files in order to classify them as images.

## Application

We have also created an application from our model that lets you upload an audiofile as .wav or .mp3 and get a classification from the 41 classes as output. To do this we have used [Voilà](https://voila.readthedocs.io/en/stable/using.html) as a jupyter server extension together with [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/examples/Widget%20List.html). By using these libraries we can create an application from the notebook which hides all the code cells. From there it is possible to use binder to deploy it for free. We got some problems when connecting it to the github repository and deploying, but it should be very possible with a little bit more time.
Right now since the application is not hosted anywhere you will have to use voilà directly from the notebook.

Just run these two lines in the notebook:

`!pip install voila` 
  
`!jupyter serverextension enable voila --sys-prefix` 
  
Then change the url from 

`http://localhost:8888/notebooks/Documents/V22/DAT255/DAT255-project/nbs/Application.ipynb` 

to 

`http://localhost:8888/voila/render/Documents/V22/DAT255/DAT255-project/nbs/Application.ipynb` 

Then you should see something like this:

![image](https://user-images.githubusercontent.com/57411743/165593385-d630301d-63bd-4216-8c52-001f069d57e3.png)

### Application with built in recording

We also experimented with adding a built in recorder so that you can chose to either upload a file or record the audio directly in the application and classify that. We made a working versio in [Application_V2.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/Application_V2.ipynb), however it did not look vey good so we decided to include both of the notebooks.

![image](https://user-images.githubusercontent.com/57411743/165594818-0b194363-f13f-44e9-b6f4-dd12cb8ba9bb.png)


There is also a notebook with the same code as in application but with some documentation as well: [Application_doc.ipynb](https://nbviewer.org/github/oyvindgrutle/DAT255-project/blob/master/nbs/Application_doc.ipynb).


## Motivation

Machine learning with audio can be used in many different situations. From simple usage like creating an application for predicting bird sounds to more complex task like audio transcription.
The model we have created might not have a direct purpose in solving a problem. However it does give a good indication on what is possible with audioclassification. We have also used our model for transfer learning which gave a better result than starting with the resnet34 from fastai. A lot of the labels in the dataset where everyday sounds and a lot of human produced noises like laughing, burping or farting. Since the model now recognized these sounds it could potentially be helpful when training a model to transcirbe spoken sentences or words where there might be background noise or other noises present.

---
