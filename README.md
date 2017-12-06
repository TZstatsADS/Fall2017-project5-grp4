# ADS Project 5: Urban Sound Classification

Term: Fall 2017

+ Group 4
+ Projec title: Urban Sound Classification
+ Team members
	+ Chen, Tiantian
	+ Li, Yijia
	+ Lin, Han
	+ Shi, Qian
	+ Zhou, Xiaoyu

+ **Project summary**: This is a project to classify unban sounds automatically with machine learning models. Our data comes from Urban Sound Dataset, which contains 1302 labeled sound recordings from 10 different classes. We extracted 193 features from these recordings, covering the features of melspectrogram, mfcc, chorma-stft, spectral_contrast and tonnetz. We split the original data and used 70% of them to train the models of GBM, Linear Regression, Random Forest, XGBoost and SVM (with 3 different kernels: linear, rbf, poly), which were applied to classify the left 30% data. Best result was produced by XGBoost, with a accuracy rate of around 75%. Apart from total accuracy rate, we also compared the training time consumed by different models and accuracy rate for each class. 

+ **Data**
	+ Source: Urban Sound Dataset
	+ Size: 1302 labeled sound recordings
	+ Format: each recording is a wav file
	+ Content: 10 classes of sounds ( air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot, jackhammer, siren, and street_music )
	+ Usage: 30% of the data is regarded as test data
	
+ **Result Comparation**
![total accuracy](https://github.com/TZstatsADS/fall2017-project5-grp4/blob/master/figs/total_accuracy.png = 150x)
	
**Contribution statement**: ([default](doc/a_note_on_contributions.md)) All team members contributed equally in all stages of this project. All team members approve our work presented in this GitHub repository including this contributions statement. 

Following [suggestions](http://nicercode.github.io/blog/2013-04-05-projects/) by [RICH FITZJOHN](http://nicercode.github.io/about/#Team) (@richfitz). This folder is orgarnized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```

Please see each subfolder for a README file.
