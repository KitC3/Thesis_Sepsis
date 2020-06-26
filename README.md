# Predicting Sepsis Using An Ensemble Of Gated Recurrent Units And Long Short Term Memory Models

Project Tilburg University

This is private repository for my thesis project. It containts the Jupyter Notebook's which were used for the project. These contain the data visualizations, the pre-processing of the data, the machine learning models and their results.

## Data
The data is originally from the [PhysioNet Computing in Cardiology challenge 2019](https://physionet.org/content/challenge-2019/1.0.0/#challenge-data) by Reyna  et  al. (2019).

The complete data for this repository can be found in this [zip](https://drive.google.com/file/d/1B7lgNuEwITl17Biud-pWKeXWv7zljaFM/view?usp=sharing) file located in my Google Drive.

## Notebooks

There are a total of 6 notebooks in this repository which can be categorised in two sections:

#### Data Visualization and Preprocessing
```bash
Sepsis Data Analysis.ipynb

Sepsis Preprocessing - Undersampling and Padding.ipynb
Sepsis Preprocessing - Missing Values.ipynb
```

The Sepsis Data Analysis.ipynb notebook contains the analysis of the dataset. Including the class distributions and the amount of missing data per variable.

The other two notebooks contain all the preprocessing steps that were done before using the data for training. In Sepsis Preprocessing - Missing Values.ipynb, the missing values in each variable are replaced/filled with "0" values. In Sepsis Preprocessing - Undersampling and Padding.ipynb, undersampling is performed on the dataset and as each time-series has a variable amount of time-steps padding is also performed.

#### Training models and Evaluating
```bash
Final_LSTM.ipynb
Final_GRU.ipynb

Final_Evaluation.ipnyb
```

In both the Final_LSTM.ipynb and Final_GRU.ipynb notebook, all the necessary single models are compiled and trained. A total of 12 models (6 GRU and 6 LSTM models) were compiled an trained as the ensembles contain 6 models. These models are saved in a single .h5 file, including the model's architecture, weights, and training configurations.

The last notebook shows the evaluation results of the single models and ensemble models based from the previous two notebooks. Metrics used for evaluation include the accuracy, precison, recall, F1 and AUC. Additionaly an AUROC (Area Under The Curve Receiver Operating Characteristics curve) is also visualized for the three ensembles, best single LSTM and single GRU models.

**As the models compiled and trained in Final_LSTM.ipynb and Final_GRU.ipynb. were saved already, these two notebooks do not have to be run again in order to run the last three notebooks as the .h5 files are located in the zip file**

## References
Reyna, Matthew A, Christopher S Josef, Russell Jeter, Supreeth P Shashikumar, M BrandonWestover, Shamim Nemati, Gari D Clifford, and Ashish Sharma. 2019. Early prediction ofsepsis from clinical data: the physionet/computing in cardiology challenge 2019.Critical CareMedicine
