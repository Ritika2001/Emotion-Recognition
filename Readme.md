# Dialogue Act Recognition

Submitted by: Ritika Nandi (rn2578)

## Introduction 
In this folder you will find a python script to normalize the features (min, max, mean pitch and intensity) accordingly by speaker and classification script to predict emotion from the acoustic-prosodic features.

## Scipts
There are 3 python scripts in the folder - 
1. `feature_extraction_analysis.ipynb` - This file contains 2 parts - Feature Extraction and Analysis. 
- The Feature Extraction section contains the code to extract speech based features using parselmouth. In order to extract the speech features, the code assumes that the original audio files are in the folder ./hw3_speech_files. The features extracted in this step are normalized by speaker.
- The Feature Analysis section contains the code to visualize the variation of these speech and features across the emotions to hypothize which features might have more importance during classification.

2. `classificationreport.py` - This is a helper file that provides a visual representation of the confusion matrix and has been used by the classification scripts.

3. `classification_experiments.ipynb` - This file contains 2 sections - Using INTERSPEECH 2009 Emotion Challenge feature set and MFCC feature set.  
- Using the Interspeech features, a Random Forest model is used to classify the emotions with Leave-one-speaker-out-validation and the weighted accuracy, weighted f1 scores and generate the confusion matrix. You will need to create a folder ./opensmile_features in the same directory where the features for each audio segment are stored as CSVs.
Then the MFCC features are used to experiment with Deep Learning models like CNNs and calculate the same metrics. For this, you will need to create a folder ./opensmile_mfcc to save the MFCC features for each audio segment as a CSV.

## Requirements
The `requirements.txt` file should list all Python libraries that your notebooks
depend on, and they will be installed using:

```
pip install -r requirements.txt
```
The requirements are - 
matplotlib==3.6.2
numpy==1.23.1
transformers==4.25.1
matplotlib==3.6.2
numpy==1.23.1
pandas==1.5.2
librosa==0.10.0.post2
keras==2.12.0
tensorflow==2.12.0
scikit-learn==1.2.0

Apart from this, you will also need to download opensmile-3.0.1-win-x64 and save it one directory up.

## Folder Structure
 ```
opensmile-3.0.1-win-x64
rn2578
|----hw3_speech_files 
     |----cc_001_anxiety_910.77_May-twenty-third.wav
     |----cc_001_anxiety_916.11_Eight-hundred-eight.wav
|----opensmile_features
     |----cc_001_anxiety_910.77_May-twenty-third.csv
     |----cc_001_anxiety_916.11_Eight-hundred-eight.csv
|----opensmile_mfcc
     |----cc_001_anxiety_910.77_May-twenty-third.csv
     |----cc_001_anxiety_916.11_Eight-hundred-eight.csv
|----classificationreport.py
|----classification_experiments.ipynb
|----feature_extraction_analysis.ipynb
|----Readme.md
|----requirements.txt
|----rn2578_responses.pdf