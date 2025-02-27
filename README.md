# 入坑指南：
前言：在实现这个项目时，遇到了几个问题，这里记录一下：
1. 需要有GPU，否则报错
2. python版本问题，需要安装python3.7 ,3.6好像也行，等会试试再改
3. 需要的几个包的版本严格安装 requirement中的说明来：但有几个需要调整，torch 安装 1.8.1 还是18.1（记不清了），torchvision 0.4.1

# Deepfake Detection

## Description

Use deep models to detect fake images. 

We trained an EfficientNet model to detect deepfake images. 
Check out this [repo](https://github.com/EndlessSora/DeeperForensics-1.0) 
to know more about deepfake images.

- Real image: 

![](./test_images/0.png)

- Fake image:

![](./test_images/1.jpeg)

## Installation

`pip install -r requirements.txt`

- Pytroch

## Usage

- ### test images using trained model

You need download the pretrained model from BaiduYun:

download link: `https://pan.baidu.com/s/16NIV5BVUITKwolQzPbj9Zw`  password:`r3i8`

And put the model(`model_half.pth.tar`) 
under `./models`. Then you can run python script as below:

`python test_images.py ./test_images/0.png ./test_images/1.jpeg`

- ### train on your own dataset

The training code is to be released.

## Cite
Please cite our code if you use this code or our models in your own work:
```
@misc{deepfake_detection,
  title={Deepfake Detection},
  author={Huang, Shiyu and others},
  howpublished={\url{https://github.com/huangshiyu13/deepfake_detection}},
  year={2020}
}
```
## Author

[Shiyu Huang](https://huangshiyu13.github.io/) (huangsy1314@163.com)

If you want to train or test your dataset using this code, 
please feel free to contact me.

## Acknowledgement

This code is based on https://github.com/rwightman/pytorch-image-models


