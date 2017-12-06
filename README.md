# ADS Project 5: Urban Sound Classification

Term: Fall 2017

+ Group 4
+ Projec title: Urban Sound Classification
+ Team members

	+ Chen, Tiantian
	+ Li, Yijia
	+ Lin, Han
	+ Shi, Qian
	+ Zhou, Xiaoyu (Presenter)

+ **Project summary**: 

This is a project to classify unban sounds automatically with machine learning models. Our data comes from Urban Sound Dataset, which contains 1302 labeled sound recordings from 10 different classes. 

We extracted 193 features from these recordings, covering the features of melspectrogram, mfcc, chorma-stft, spectral_contrast and tonnetz. We splitted the original data and used 70% of them to train the models of GBM, Linear Regression, Random Forest, XGBoost and SVM (with 3 different kernels: linear, rbf, poly), which were applied to classify the left 30% data. Best result was produced by XGBoost, with a accuracy rate of around 75%. Apart from total accuracy rate, we also compared the training time consumed by different models and accuracy rate for each class. 

**Our main file can be found [here](doc/main_file.pdf), and our ppt can be found [here](doc/presentation.pdf).**

+ **Data**
	+ Source: [Urban Sound Dataset](https://serv.cusp.nyu.edu/projects/urbansounddataset/)
	+ Size: 1302 labeled sound recordings
	+ Format: each recording is a wav file
	+ Content: 10 classes of sounds ( air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot, jackhammer, siren, and street_music )
	+ Usage: 70% of the data is regarded as training set, while the rest of the data is used as test set

+ **Feature**
	+ Tool: Librosa library in Python
	+ Methods: 
		+ melspectro gram (compute a Mel-scaled power)
		+ mfcc: Mel-frequency cepstral coefficients
		+ chorma-stft: chromagram from a waveform/power spectrogram
		+ spectral_contrast: Compute spectral contrast, using method
		+ tonnetz: Computes the tonal centroid features (tonnetz)
	+ Output: Matrix of 1102 rows, 193 columns

+ **Model**
        
	+ GBM
	+ Logistic Regression
	+ Random Forest
	+ XGBoost
	+ SVM (linear, RBF kernel, polynomial kernel)


+ **Result Comparation**
   + Total accuracy and traing times:
![total accuracy and time](figs/put_together.png)
   + Accuracy for each class:
![accuracy for each class](figs/acu_bar.png)
![accuracy for each class](figs/acu_bubble.png)
   + Accuracy table:
![accuracy table](figs/acu_table.png)

+ **Improvement**
    + Use a larger dataset on the [official website](https://serv.cusp.nyu.edu/projects/urbansounddataset/) which contains more than 8000 audio records with these 10 different classes. Intuitively, more data available,  more accurate for model performs.
    + Set up a more complex CNN with at least 10 layers, and with some other techniques, such as adding zero-padding or dropout layer to classify those audios.
    + Try to use different combinations within those five kinds of features we extracted.  We have assumed that perhaps some kinds of the features are much more outstanding than others. So why not try to ignore those "unuseful" features, at some points, reduce dimensions, and train the model on the subset of the features. The result could be exciting, or not.
    + Try to extract other kinds of features.
	
+ **Contribution statement**: All team members approve our work presented in this GitHub repository including this contributions statement.
    + Han Lin
    
        + Downloaded 16 GB audio file from Urban Sound website.
        + Extracted mfccs,chroma,mel,contrast,tonnetz features from raw audio files using librosa library in python.
	+ Implemented Logistic regression model and 2-layer neural network model.
	+ Organized main file.
	+ Organized Github.
	+ Drew accuracy comparison draft plot.
	

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

**Reference**: 

[Urban Sound Classification](http://aqibsaeed.github.io/2016-09-03-urban-sound-classification-part-1/)

[Librosa](http://librosa.github.io)
