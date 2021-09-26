# Recommendations-with-IBM-Watson
A recommendation engine that would suggest articles, users and article titles interacted with for each of the specific case of article id and user id provided

## Table of Contents
1. [Project Motivation](#motivation)
2. [File Descriptions](#files)
3. [Instructions](#instructions)
4. [Results](#results)
5. [Licensing, Authors & Acknowledgments](#licensing)

## Project Motivation<a name="motivation"></a>

The project is offered by Udacity. The objective of this project is to make a recommendation engine using the IBM-watson user-article interaction data. Rank-based recommendation and collaborative filtering were used to make recommendation of articles and article_ids. 


<img src="https://render.githubusercontent.com/render/math?math=IRR=\frac{purch_{treat}}{cust_{treat}} - \frac{purch_{ctrl}}{cust_{ctrl}}">



<img src="https://render.githubusercontent.com/render/math?math=NIR = (10\cdot purch_{treat} - 0.15 \cdot cust_{treat}) - 10 \cdot purch_{ctrl}">

## File Description<a name="files"></a>

These are the files in the project.

```
1. user_item_interactions.csv               -file containing the dataset for users(email), and article_ids
2. article_community.csv                    -file containing further data on articles with doc_body, doc_description that could be helpful in content recommendation
3. Recommendaions with IBM.ipynb            -jupyter file containing all the analysis along with code and explanations
4. project_tests.py                         -file written in python to verify the assert tests written in dicionaries format
5. top_5.p, top_10.p, top_20.p              -pickle files with results saved to verify the assert tests
6. user_item_matrix.p                       -pickle file saved of user_article (user_item) interaction to be imported later into project

```

## Instructions<a name="instructions"></a>

In order to run the project place the files in the same directory. There aren't any special libraries needed to run this project. The standard ones needed are Pandas, numpy, scipy and sklearn. Make sure to place the data files (.csv) in the folder labeled data. Or change the path as necessary

## Results<a name="results"></a>

In the implementation of this recommendation engine, a combination of collaborative filtering and rank based recommendation was used to make suggestions of specific article_ids and article titles. Rank based recommendation are given using top recommendation for either article_ids or article titles that have the most interaction with the user. 

Collaborative filtering part gives recommendation of articles and article_ids using similarity measurement index. In the first part, neighbourhood assignments were recommended as most similar articles/article_ids based on the measurement of similarity index (obtained through dot product). In the second phase, articles/article_ids were suggested based on the interaction of users and removing the common suggestions obtained in the neighbourhood measurement phase. In the third phase, the articles/article_ids were suggested based on decreasing measurements of both similarity index as well as number of user-article interactions. The implementation of content based recommendation has been left for another time and can be accomplished using NLTK to deconstruct the data of article_community.csv, making new columns and then getting content based information out of each article_id

In the end implementation of FUNKSVD is used to suggest accuracy of the model on the test data and potential A/B testing implementation route is discussed. 

## Licensing, Authors & Acknowledgments<a name="licensing"></a>

Incredibly grateful to the team at Udacity as well as IBM for providing the data. 
