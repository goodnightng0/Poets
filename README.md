# Topic: Can the gender of poets be classified based on their poem content/styles?
Project for our Data Science Study #Team 통소여

## Data
- Poetry data downloaded from [Kaggle](https://www.kaggle.com/jatindersehdev/poetry-analysis-data)    
- We manually updated the poetry gender with data crawling


## Methods
We implemented _two versions_, one including stopwords and one with stopwords excluded.
Normally in textmining, stopwords are excluded.
However, because poems tend to showcase emotions through various words, we decided to look into both versions.

> 1. Random Forest
> 2. AdaBoostRegressor
> 3. KNN
> 4. Naive Bayes
> 5. SVC
#### The detailed manners of each method are described carefully in our files: /classification/ (View .ipynb or download our html file)

## Result Interpretation
```
We have constructed quite a few models and tried updating our parameter values but the accuracy was only around 0.5~0.6
Considering that we only have two groups, it is a very low value and we concluded that our analysis was not significant.
Also, there was not much of a difference whether or not we included stopwords.
(The accuracy is saved in  /data/accuracy.csv)
```
### Why?
```
There could be a couple reasons for this problem

First, we used 3000 poets for 15000 data(poems). We could have tried to obtain more data.
Also, poems are very short in length, unlike novels or scripts that are normally used in textmining.

Therefore, these conditions might have caused overfitting.
```
### Lessons and to-think-abouts
Preparing for this hackathon, we have learned that preprocessing datas are one of the most important levels in datamining.   
As it could distort our results, it should be approached with caution when it comes to removing values or filling NA blanks.   
Also we concluded that classifying natural language into two groups is difficult than it seems, becuase language has many unpredictable & untangible factors.

- Future think-abouts: Could it be improved by supervised & unsupervised learning?
