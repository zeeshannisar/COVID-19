# Detecting COVID-19 in X-ray Images Using Different Pretrained-Networks in Tensorflow 2.x.
The Corona Virus Disease 2019 (COVID-19) pandemic continues to have an upsetting effect on the health and well-being of the global population. A critical step in the fight against COVID-19 is effective screening of infected patients, with one of the key screening approaches being radiological imaging using chest radiography. It was found in early studies that patients present abnormalities in chest radiography images that are characteristic of those infected with COVID-19 as discussed in a recent [[Paper]](https://arxiv.org/abs/2003.09871). Therefore, in this Repository I have tested different Pretrained Networks for the detection of COVID-19 cases from chest radiography images that is open source and available to the general public. **Finally a Novel Method will be introduced to get the maximum of Positive Predicted Values from these Pretrained Networks.**

## Table of Contents
  + Datset Description
    + Dataset 01
    + Dataset 02
  + Pretrained Networks for COVID-19 Detection
    + VGG19
    + AlexNet
    + Inception V3
    + ResNet-18
    + DenseNet-121
    + Google-Net
  
### Dataset Description:
#### Dataset 01:
This dataset is the first version introduced by the authors of the [[Paper]](https://arxiv.org/abs/2003.09871). I have write a python script to categorize each X-ray image to a separate Class as below.

| Category    | Number of Patients | Number of Images |
| --------    | ------------------ | ---------------- |
| 0: Normal   | 1203               | 1583             |
| 1: Bacteria | 931                | 2786             |
| 2: Viral    | 660                | 1504             |
| 3: COVID-19 | 45                 | 76               |


This dataset can be accessed at [Here]()
