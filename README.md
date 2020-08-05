

# Classifying Emotions With Audio
This project was started as the capstone project for BrainStation's data science diploma program.
#### -- Project Status: [Active]

## Project Intro/Objective
The purpose of this project is to explore techniques that can be used to classify emotions based on audio data, particulaly using recordings of people's voices.

### Methods Used
* Feature Extraction (MFCC, GFCC, LFCC, raw audio, etc.)
* Machine Learning
* Neural Networks (Dense, Convolutional, Recurrent)
* Probabilistic Voting

### Technologies
* Python
* Jupyter
* Pandas, Numpy, Librosa
* SKLearn, Keras
* VSCode

## Project Description

* The primary data used in this project was sourced from the [Toronto emotional speech set](https://dataverse.scholarsportal.info/dataset.xhtml?persistentId=doi:10.5683/SP2/E8H2MF) (TESS) and the [Surrey Audio-Visual Expressed Emotion Database](http://kahlan.eps.surrey.ac.uk/savee/) 
* A few audio based features were extracted to model with, including the mel frequency cepstral coefficients (MFCCs), the gammatone frequency coefficients (GFCCs), and the raw audio resampled at 11 kHz. The MFCCs and GFCCs were averaged over time so that each sample would have a set number of features. 40 coefficients was found the be the most effective for modelling.
* There were seven target classes, each for the seven primary emotions: anger, disgust, fear, sadness, neutral, happy, and surprised.
* After data cleaning and dealing with class/gender imbalances, there were 840 audio files to be used for modelling, with 70% used to train the models and 30% used to test.
* Multiple models were tested to explore which feature/model selection would result in the highest classification accuracy. The most successful models were based on the MFCCs, and included an RBF kernel support vector machine, random forest, dense neural network, and 1D convolutional neural network.
* Challenges were faced training models based on the raw audio of each file, and using recurrent neural networks to effectively train on the data.
* The final combined accuracy of the top performing models was around 92%.

## Next Steps

* More data!

## Getting Started

1. Clone this repo or download project files [here](https://www.dropbox.com/sh/52evb9pxryagkfq/AAAh-5tyVTRIYN4Q7AQj1cJJa?dl=0)
2. Create a virtual environment and install required packages with _requirements.txt_. If you need help with this refer to [this guide](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)    
3. Open the _Capstone Final Notebook.ipynb_ in a Jupyter Notebook
4. Change the PATH variable in the first code cell in the notebook to where the project folder resides on your computer.
5. Run everything if you wish. Neural networks will be loaded from saved models, you can train them yourself if you uncomment the _model.fit_ cells in the neural network sections.
6. Be sure to check out the demo near the end of the project where you can have your own emotion predicted from the sound of your voice! 

Feel free to contact me at [cole.slatt@gmail.com](cole.slatt@gmail.com) if you have any questions
