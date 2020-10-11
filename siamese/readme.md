### Siamese Neural Network
---

These were experimets i have done in the time while i am waiting for recommendation letter from my professors 

#### Dataset
I am going to conduct my experiments from kaggle dataset - [http://https://www.kaggle.com/tawsifurrahman/covid19-radiography-database](http://https://www.kaggle.com/tawsifurrahman/covid19-radiography-database)
The dataset consists of chest X-ray images of covid-19 positive cases along with normal and Viral Pneumonia images.

-  covid-19 positive images - 219
-  normal images                 - 1341
-  viral pneuomonia images - 1345

*Their is clearly class imbalance problem here. Instead to spend a lot of time before tackle this problem i have tried to build a model with imbalanced data to see how it goes and the results were promising.*


------------

1. The network is pretrained on ImageNet dataset and transfer learning on 2905 chest x-ray images.

2. Siamese Neural Network take two seperate images as inputs which are passed through identical neural networks.

3. 80% dataset is used for training and remaining 20% for validation

------------

* The network is trained in two stages, first the resnet is trained with freezing previous layers and training head with high cyclical learning rate[link](https://arxiv.org/pdf/1803.09820.pdf). later all the layers were unfreezed and trained with small learning rate.

|  models | accuracy   |
| ------------ | ------------ |
|  Resnet18 | 0.922547  |
|  Resnet34 | 0.946644 |
|  Resent50 | 0.979346  |




