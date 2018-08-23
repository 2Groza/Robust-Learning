# Robust Learning via AutoEncoder Pre-training (AEP)

## 1. in unsupervised classification task

I got this idea first in a previous project of "unsupervised star-galaxy classification", in which I used 100,000 unlabled star/galaxy images to train a model and then used that model to predict 140,000 labled images and got an overall AUC over 0.91.

Without such pretraining method, the biggest problems I met in training process was the unstability and time consuming process of hyperparameter tuning. Those problems were solved in the ways below:
- Fast and even free in hyper-parameter tuning: the AEP net is always easy to train for its purpose is to reproduce the original inputs. And this process can greatly reduce the dimensions of classification problems. In my experiments, I use AEP to do dimension-reduction from 64x64x5 to only 30 units. 

- By pre-training using AutoEncoders with BatchNormalization, the distribution of input datas of further network is tuned automatically to a much more consistent shape, as is shown below:

the first four images shows the original pixel value histograph while the last four shows the histograph after using AEP. In experiments, AEP brought about significant improvement in the performance of unsupervised learning.

<img src="https://github.com/2Groza/images/blob/master/robustlearning/bf6.png" width=200 height=150 /><img src="https://github.com/2Groza/images/blob/master/robustlearning/bf7.png" width=200 height=150 /><img src="https://github.com/2Groza/images/blob/master/robustlearning/bf8.png" width=200 height=150 /><img src="https://github.com/2Groza/images/blob/master/robustlearning/bf9.png" width=200 height=150 />

<img src="https://github.com/2Groza/images/blob/master/robustlearning/aft6.png" width=200 height=150 /><img src="https://github.com/2Groza/images/blob/master/robustlearning/aft7.png" width=200 height=150 /><img src="https://github.com/2Groza/images/blob/master/robustlearning/aft8.png" width=200 height=150 /><img src="https://github.com/2Groza/images/blob/master/robustlearning/aft9.png" width=200 height=150 />


## 2. in segmentation task with limited data quantity


