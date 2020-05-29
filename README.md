[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

[![python3](https://img.shields.io/badge/python3-v3.8-blue?style=for-the-badge&logo=python)](https://www.python.org)

# Color-Convolution
An experiment to validate one of my ideas of an approach to train a CNN.

### Description
Generally CNNs that process RGB or images in some other format run the same convolution filter on each channel. This might cause the network to not consider the resulting color of each pixel. So I tried using a conv3d layer instead of conv2d to get a 3*3*3 kernel with each channel getting a unique 3*3 kernel and the correlation output of the convolution extending to all the 3 channels.

## Dataset
The dataset considered is the cifar-10 dataset built in the tensorflow.keras.dataset module. I selected this dataset because it has RGB images and small to test on.
![analysis](https://github.com/sagnik106/Color-Convolution/blob/master/resources/data_analysis.png)
![classes](https://github.com/sagnik106/Color-Convolution/blob/master/resources/dataclass.png)
## Requirements
* Numpy 1.18.3
* Matplotlib 3.2.1
* Tensorflow 2.2

## Models
The model has been taken from [keras.io]() for easy comparision.<br/>
Normal model<br/>
![2D](https://github.com/sagnik106/Color-Convolution/blob/master/resources/2d.png)
Improved model<br/>
![3D](https://github.com/sagnik106/Color-Convolution/blob/master/resources/3d.png)

## Results
The Maximum validation accuracy attained by the proposed model is 0.89%. For datasets having more resolution better improvement is expected
![metrics](https://github.com/sagnik106/Color-Convolution/blob/master/resources/metrics.png)

## File Cofiguration
* [cifar10.ipynb]() - Jupyter notebook which has the analysis of dataset along with the declaration and training of the model
* [resources/](https://github.com/sagnik106/MNIST-c-GAN/blob/master/resources/) - Github README resources