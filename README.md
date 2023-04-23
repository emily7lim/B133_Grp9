# Welcome to spotify-analysis repository

## About

This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on songs from 3 datasets merged.

1. This data is obtained from [The Spotify API](https://developer.spotify.com/documentation/web-api)

2. This dataset consists of [lyrics](https://www.kaggle.com/datasets/nikhilnayak123/5-million-song-lyrics-dataset) from kaggle dataset. 

3. This dataset consist of [Spotify popular songs](https://www.kaggle.com/datasets/dhruvildave/spotify-charts) which contains viral50 and top200 songs on Spotify.

---
## Table of Contents:
1. [Data Fetching and Cleaning](#1-Data-Fetching-and-Cleaning)
2. [Exploratory Data Analysis](#2-Exploratory-Data-Analysis)
3. [Machine Learning](#3-Machine-Leanring)
4. [Data Driven Insights](#4-Data-Driven-Insights)
5. [Fine Tune Model](#5-Fine-Tuning-model)
6. [Models Used](#6-Models-Used)
7. [Conclusion](#7-Conclusion)
8. [References](#8-References)

---

## Problem Definition

**The Dataset**: [Spotify popular songs](https://www.kaggle.com/datasets/dhruvildave/spotify-charts) which contains viral50 and top200 songs on Spotify.

**Our Question**: Each day, countless songs are released on Spotify. It makes us wonder what songs get popular in a day, and stay up in the trending chart for days? Is it the lyrics, the unique elements of the songs, luck or publication from social media that makes a song stand out? We were intrigued by this question. Therefore, our project's goal is to create a classification model to determine if a song will be on trend, which would help musicians produce more popular and applealing music.


## Notebooks

We will be using (positive,popular) and (negative,non-popular) interchangeably. 

For detailed walkthrough, please view the source code in order from:

### 1. Data Fetching and Cleaning

> 1.1 [Data Fetching and Cleaning](https://github.com/emily7lim/B133_Grp9/blob/main/1DataProcessing.ipynb) 

Obtaining dataset from kaggle and spotify API. Preparing positive and negative data to be merged by extracting necessary features

### 2. Exploratory Data Analysis

> 2.1 [EDA](https://github.com/emily7lim/B133_Grp9/blob/main/2.1EDA.ipynb)

Exploring our datasets and check if there is any relation that leads to a song being popular.

> 2.2 [EDA based on Dimension Reduction](https://github.com/emily7lim/B133_Grp9/blob/main/2.2EDA_dimensionReduction.ipynb)
        
Use tSNE and Davies Bouldin Score to better measure the relationship between features and popularity.
 

### 3. Machine Learning

> 3.1 [Classic Models](https://github.com/emily7lim/B133_Grp9/blob/main/3.1MachineLearning.ipynb) 

We started with classic machine learning models such as svm, logistic regression, random forest and decision tree to build the prediction model.

> 3.2 [Bert Only Baseline Model](https://github.com/emily7lim/B133_Grp9/blob/main/3.2BERTOnlyBaselineModel.ipynb)

However, we are not completely satisfied with it, we want a better model. Hence, we attempted to use lyrics data and NLP methods to obtain a more accurate model. 

To construct a baseline model, we employed Bert exclusively to predict whether a song would become popular or not. Our model consists of a DistilBert model combined with MLP layer, followed by a sigmoid function and BCELoss.

> 3.3 [Bert and Other Features Prediction Model](https://github.com/emily7lim/B133_Grp9/blob/main/3.3BERTAndOtherFeaturesModel.ipynb)

After establishing the baseline model, we sought to create a model that would leverage both lyrics and additional data. Our new model, hence, will concatenates the output from Bert with other features, enabling a more comprehensive prediction of song popularity.

### 4. Data Driven Insights
> 4.1 [Lyrics' effect](https://github.com/emily7lim/B133_Grp9/blob/main/4.1Insights_HowLyricsAffectSongs.ipynb)

Determine the effect that lyrics-only have on deciding if a song is popular. 
> 4.2 [Does one feature have an impact on the entire song: Energy](https://github.com/emily7lim/B133_Grp9/blob/main/4.2Insights_HowOneFeatureAffectPopularity_Energy.ipynb)
        
Selecting a random feature, energy to determine if changing only one will affect the prediction.

> 4.3 [Does one feature have an impact on the entire song: Liveness](https://github.com/emily7lim/B133_Grp9/blob/main/4.2Insights_HowOneFeatureAffectPopularity_Liveness.ipynb)

Selecting another feature, liveness to determine if changing only one will affect the prediction.

### 5. Fine-tuning model
> 5.1 [How Dropout affect model training](https://github.com/emily7lim/B133_Grp9/blob/main/5.1HowDropoutAffectModels.ipynb)
    
This notebook is similar to 3.3 except that we removed the dropout here to see how dropout layers can increase the models' performance.

> 5.2 [How Learning Rate affect model training](https://github.com/emily7lim/B133_Grp9/blob/main/5.2HowLearningRateAffectModels.ipynb)

This notebook is similar to 3.2 except that the learning rate is 1e-5 to see how learning rate  affect the  training process.


### 6. Models Used

1. Logistic Regression
2. SVM
3. Random Forest
4. Decision Tree
5. BERT
6. BERT+MLP

### 7. Conclusion

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

### 8. References

- https://developer.spotify.com/documentation/web-api/reference/get-audio-features
- https://huggingface.co/distilbert-base-uncased
- https://en.wikipedia.org/wiki/Pitch_class
- https://www.kaggle.com/code/vhtrieu/spotify-charts-analysis
- https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html
