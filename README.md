# Steam-Review-Analysis
### Steam Review Topic Modeling and Classification
#### Author: Lechuan Qiu, Boyang Wei, Mengzhi Zhou

### Overview
This project focuses on using natural language processing techniques: Topic Modeling and Text Classification on reviews of Steam best selling games since February 2019 to help game developers better understand the trending topics, game properties and potential problems/improvements from the gaming community.

### Data
Review of Steam’s best selling games since February 2019, which contains over 400,000 rows with 8 columns: 
1. date posted by reviewer (date_posted)
2. how many people think this comment funny(funny)
3. how many people think this comments helpful(helpful)
4. how many hours does reviewer plays(hour_played)
5. early access review or not(early_access)
6. if the game is recommended or not (recommendation)
7. game review comments(review) 
8. title(title)

Link: https://www.kaggle.com/luthfim/steam-reviews-dataset

### Methods and Steps
The projects contain three parts: Exploratory Data Analysis, Topic Modeling and Classification.

#### Exploratory Data Analysis (Project 2 - EDA.ipynb)
This part contains codes and visuals to explore the original dataset from Kaggle Competition, and process/clean the data accordingly for the later parts.
The cleaning mainly consists of: 
1. remove missing values
2. remove not-helpful comments 
3. remove stop words
4. remove customized frequent words
5. remove non-ASCII encoded characters

#### Topic Modeling (Project 2 - Topic Modeling.ipynb) 
This part contains codes and visuals to learn best number of topics by coherence values, subset the entire dataset and extract the topics by subsets accordingly. The subsets consists of:
1. recommended reviews
2. not-recommended reviews
3. 'PUBG reviews' (top 1 trending game)
4. 'TGA 5' reviews (top 2 trending game)

The topics from each of the section could reflect the topics gamers are discussing accordingly, and more details and explanation could be found in the notebook above.

Note: mallet-2.0.8 needed for visualize the topic modeling results

#### Text Classification (Project 2 - Text Classification.ipynb)
This part contains codes and visuals of training a recurrent neural networks to classify the reviews based on recommendation (recommended vs not-recommended)
Specifically, this part converts text with word embeddings to fit into a customized neural network with:
1. 1000 by 100 embedding layer
2. random dropout rate of 0.2
3. LSTM layer
4. dense layer for binary classification

The final accuracy on testing set is around 0.79; more visuals regarding to training/testing loss and accuracy with different epochs could be found in the notebook above.

### Results:
The presentation poster could be found here
More details could be found in the jupyter notebooks above.


