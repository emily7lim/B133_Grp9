# Welcome to spotify-analysis repository

## About

This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on songs from 3 datasets merged.

1. This data is obtained from [The Spotify API](https://developer.spotify.com/documentation/web-api)

2. This dataset consists of [lyrics](https://www.kaggle.com/datasets/nikhilnayak123/5-million-song-lyrics-dataset) from kaggle dataset. 

3. This dataset consist of [popular songs](https://www.kaggle.com/datasets/dhruvildave/spotify-charts) which were in viral50 and top200.

## Problem Definition

- Are we able to analyze trends in songs and use previous data to predict which song will be popular?
- Which model would be the best to predict it?

---
### Table of Contents:
1. [Data Processing](#1-Data-Processing)
2. [Data Visualisation](#2-Data-Visualisation)
3. [Dimensionality Reduction](#3-Dimensionality-Reduction)
4. [Machine Learning](#4-Machine-Leanring)
5. [Insights](#5-Clustering)
6. [Fine Tune Model](#6-Fine-Tuning)
7. [Models Used](#7-Models-Used)
8. [Conclusion](#8-Conclusion)
9. [References](#9-References)

---

### Notebooks

We will be using (positive,popular) and (negative,non-popular) interchangeably. 

For detailed walkthrough, please view the source code in order from:

### 1. [Data Processing](https://github.com/emily7lim/B133_Grp9/blob/main/1DataProcessing.ipynb)

Obtaining dataset from kaggle and spotify API. Preparing positive and negative data to be merged by extracting necessary features

### 2. [Data Visualisation](https://github.com/emily7lim/B133_Grp9/blob/main/2.1EDA.ipynb) 

Exploring our datasets and check if there is any relation that leads to a song being popular.

### 3. [Dimension Reduction](https://github.com/emily7lim/B133_Grp9/blob/main/2.2EDA_dimensionReduction.ipynb)

 Use tSNE and Davies Bouldin Score to better measure the relationship between features and popularity.

### 4. Machine Learning

> 4.1 [Classic](https://github.com/emily7lim/B133_Grp9/blob/main/3.1MachineLearning.ipynb) 

> 4.2 [Bert Only Baseline](https://github.com/emily7lim/B133_Grp9/blob/main/3.2BERTOnlyBaselineModel.ipynb)

> 4.3 [Bert and Other Features](https://github.com/emily7lim/B133_Grp9/blob/main/3.3BERTAndOtherFeaturesModel.ipynb)

        
Models taught in SC1015 were utilised here. Use pretrained model Bert to do transfer learning on lyrics to predict if a song will be popular. We also add on to 3.2 by adding other features to the model.

### 5. Insights
> 5.1 [Lyrics' effect](https://github.com/emily7lim/B133_Grp9/blob/main/4.1Insights_HowLyricsAffectSongs.ipynb)

Determine the effect that lyrics-only have on deciding if a song is popular. 
> 5.2 [Change Feature: Energy](https://github.com/emily7lim/B133_Grp9/blob/main/4.2Insights_HowOneFeatureAffectPopularity_Energy.ipynb)
        
Selecting a random feature, energy to determine if changing only one will affect the prediction.
> 5.3 [Change Feature: Liveness](https://github.com/emily7lim/B133_Grp9/blob/main/4.2Insights_HowOneFeatureAffectPopularity_Liveness.ipynb)

Selecting another feature, liveness to determine if changing only one will affect the prediction.
### 6. Fine-tuning model
> 6.1 [Removing Dropout](https://github.com/emily7lim/B133_Grp9/blob/main/5.1HowDropoutAffectModels.ipynb)
    
This notebook is similar to 3.3 except that we removed the dropout here to see how dropout layers can increase the models' performance
> 6.2 [Learning Rate](https://github.com/emily7lim/B133_Grp9/blob/main/5.2HowLearningRateAffectModels.ipynb)

This notebook is similar to 3.2 except that the learning rate is 1e-5 to see how learning rate  affect the  training process


### 7. Models Used

1. Logistic Regression
2. SVM
3. Random Forest
4. Decision Tree
5. BERT

### 8. Conclusion

- Lyrics play a crucial role in determining a song's popularity. 
- A successful song is not determined by only one feature but consists of many features such as loudness, energy, acousticness etc.
- Using lyrics, features and Bert as a model achieved the best result.

### What did we learn from this project?

- Identifying the optimal learning rate is crucial
- Early stopping is essential
- Incorporating dropout layers is vital for model generalization
- Merging of multiple datasets help to enrich data and enhance model
- Having a high learning rate does not necessarily lead to a better result as overfitting may occur.

### Contributors

- @EricFan2002
- @serenawjw
- @emily7lim

### 9. References

- https://developer.spotify.com/documentation/web-api/reference/get-audio-features
- https://huggingface.co/distilbert-base-uncased
- https://en.wikipedia.org/wiki/Pitch_class
- https://www.kaggle.com/code/vhtrieu/spotify-charts-analysis
- https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html
