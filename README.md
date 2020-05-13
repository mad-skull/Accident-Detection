# Model Overview
1 . For this project we have tweaked Densenet-161 architecture

Dense Convolutional Network (DenseNet), connects each layer to every other layer in a feed-forward fashion. Whereas traditional convolutional networks with L layers have L connections - one between each layer and its subsequent layer - our network has L(L+1)/2 direct connections. For each layer, the feature-maps of all preceding layers are used as inputs, and its own feature-maps are used as inputs into all subsequent layers. DenseNets have several compelling advantages: they alleviate the vanishing-gradient problem, strengthen feature propagation, encourage feature reuse, and substantially reduce the number of parameters.

The 1-crop error rates on the imagenet dataset with the pretrained model are listed below.

Model structure    Top-1 error    Top-5 error

densenet121  :  25.35   : 7.83

densenet169  :  24.00   : 7.00

densenet201  :  22.80   : 6.43

densenet161  :  22.35   : 6.20

# Prerequisite 

Download anaconda from here https://www.anaconda.com/distribution/#download-section

1. Pytorch 

> conda install pytorch torchvision cudatoolkit=10.1 -c pytorch


2. OpenCV 

> conda install -c conda-forge opencv

3. Dataset of accident/non-accident images 

>  https://drive.google.com/open?id=1o0D7vnGUZHS72is6n1jV1ge2BDfObzVi

4. Pretrained Model binary file

>  https://drive.google.com/open?id=1AnJSogx65iyfIG0cSm5D15xfTGJzst8d


5.  A proper php-language environment like xampp,remove htdocs folder and replace that with htdocs in this repo

6. Clone or Download this repo 

> git clone https://github.com/mad-skull/accident-detection.git

# DEMO

***1.accident***

![alt text](https://raw.githubusercontent.com/mad-skull/accident-detection/master/assets/5.gif)

***2.Non-accident***

![alt text](https://raw.githubusercontent.com/mad-skull/accident-detection/master/assets/6.gif)


# Train 

Go to bash/cmd and type

python train.py

# Tensorboard visual 
**1. Traning set 
![alt text](https://raw.githubusercontent.com/mad-skull/accident-detection/master/assets/4.png)
2. Validation set**
![alt text](https://raw.githubusercontent.com/mad-skull/accident-detection/master/assets/2.png)
**3.Number of corercts v/s epochs**
![alt text](https://raw.githubusercontent.com/mad-skull/accident-detection/master/assets/3.png)
# Test/Accuracy

Go to bash/cmd and type

> python test.py

# Test on video

> python evaluate.py

# Test on Webcam

> python livewebcam.py
# Result

![alt text](https://raw.githubusercontent.com/mad-skull/accident-detection/master/assets/1.png)

The model reaches a classification accuracy of 86.00% accuracy on a randomly sampled test set, composed of 20% of the total amount of video sequences from our dataset. Will re-train this model when we have a good GPU and somre data .
