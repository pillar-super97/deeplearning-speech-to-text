# Speech Recognition for African language

We are going to build deep learning model to convert African language speech to text format in this project.

## Table of Content
- [Introduction](#introduction)
- [Install](#instalation)
- [Data](#data)
- [Notebooks](#notebooks)
- [Scripts](#scripts)
- [Technologies used](#technologies-used)

### Introduction
A bread production company wants to deploy an intelligent form that collects nutritional information of wheat bought at markets in some different countries in Africa.

The design of this intelligent form requires selected people to install an app on their mobile phone, and whenever they buy wheat, they use their voice to activate the app to register the list of items they just bought in their own language. The intelligent systems in the app are expected to live to transcribe the speech-to-text and organize the information in an easy-to-process way in a database.

It is our obligation to create a deep learning model capable of converting speech to text. The model we create should be precise and resistant to background noise.
This project was created during the fourth week of the Machine Learning training session at 10Academy.

### Instalation

- **Install Required Python Moduls**
``` 
git clone https://github.com/pillar0124/deeplearning-speech-to-text.git
cd speech_to_text
pip install -r requirements.txt
```

- **Jupiter Notebook**
```
cd notebooks
jupyter notebook
```

- **Model Training ui (Not implemented yet)**
```
mlflow ui
```

- **Dashboard (Not implemented yet)**
```
streamlit run app.py
```

### Data

The folder is being tarcked with DVC and the files are only shown after cloning and setting up locally. The sub-folder ```AMHARIC``` contain ```training``` and ```testing``` files for our model. Both files contain similar file structure.

- **```wav/```** : a folder containing all audio files
- **```text```** : file contining the metadata (audio file name and cropsonding transcription)
- **```spk2utt```**, **```trsTest.txt```**, **```utt2spk```**,  **```wav.scp```** : these are files provided with the dataset, Currently they don't have a purpose but could be used for future analysis.


### Notebooks

- Preprocessing.ipynb: all the data preprocessing done here before model training.

### Scripts

- data_cleaning.py: contain all the data cleaning and modularizing functions.
- data_viz.py: contain all the visualization related functions.

### Technologies used

- [DVC](https://dvc.org/) : Remote Data Storage
- [MLflow](https://www.mlflow.org/): Model training and visualization
- [CML](https://github.com/iterative/cml): Display Model result and usefull information during pull requests
- [Streamlit](https://streamlit.io/): Display Web interface and dashboard