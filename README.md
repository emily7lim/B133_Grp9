# Welcome to spotify-analysis repository

## About

This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on songs from 3 datasets merged.

1. This data is obtained from [The Spotify API](https://developer.spotify.com/documentation/web-api) 

2. This dataset consists of [lyrics](https://www.kaggle.com/datasets/nikhilnayak123/5-million-song-lyrics-dataset) from kaggle dataset. 

3. This dataset consist of [popular songs](https://www.kaggle.com/datasets/dhruvildave/spotify-charts) which were in viral50 and top200.

For detailed walkthrough, please view the source code in order from:

1. [Data Processing](https://github.com/emily7lim/B133_Grp9/blob/main/1DataProcessing.ipynb)

2. Data Visualisation
    - 2.1  [EDA](https://github.com/emily7lim/B133_Grp9/blob/main/2.1EDA.ipynb)
    - 2.2  [Dimension Reduction](https://github.com/emily7lim/B133_Grp9/blob/main/2.2EDA_dimensionReduction.ipynb)

3. Machine Learning
    - 3.1 [Classic]()
    - 3.2 [Bert Only Baseline]()
    - 3.3 [Bert and Other Featres]()

4. [Change of Learning Rate]()
  
## Contributors

- @EricFan2002
- @serenawjw
- @emily7lim

## Problem Definition

- Are we able to analyze trends in songs and use previous data to predict which song will be popular?
- Which model would be the best to predict it?

## Models Used

1. Logistic Regression
2. SVM
3. Random Forest
4. Decision Tree
5. BERT

## Conclusion

- Lyrics play a crucial role in determining a song's popularity. 
- A successful song is not determined by only one feature but consists of many features such as loudness, energy, acousticness etc 
- Using lyrics, features and Bert as a model achieved the best result

## What did we learn from this project?

- Identifying the optimal learning rate is crucial
- Early stopping is essential
- Incorporating dropout layers is vital for model generalization
- Merging of multiple datasets help to enrich data and enhance model

## References

- https://developer.spotify.com/documentation/web-api/reference/get-audio-features
- https://huggingface.co/distilbert-base-uncased

- 