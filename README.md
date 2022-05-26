# Project Name
This project is related to my first data science blog post, written as part of my Udacity data science nanodegree education. The blog post can be found [here](https://medium.com/@julienflandre/can-robots-be-sommeliers-cf8134302680). The project consists in analysing data about red and white Vinho Verde wines and building a machine learning algorithm to class wines by quality level.

## General Information
This repository contains the two original csv files used for the analysis and the Jupyter Notebook with the code to follow along the process.

I start by stacking the two datasets into one by adding a style column to differentiate the red and white wines. I then run some exploratory data analysis to get familiar with the dataset and come up with the three following questions that I want to answer: <br>
**What are the strongest correlations present amongst variables?**<br>
**What are the main differences between white and red wines in the dataset?**<br>
**Is it possible to accurately class wine by quality based on their chemical makeup?**<br>

I then proceed in visualising a correlation matrix that indicates that they are no strong correlations amongst unnrelated features except one negative between alcohol and density.

Here is a table to answer the second question: <br>
![wine comparison table](https://miro.medium.com/max/800/1*OXOy0Cee0dxqdjZywL0S_w.png)

And finally I go on to train a ML model to predict wine quality levels based on all other features. A quick look at features boxplots reveal that a few of them have rather significant outliers which led me to choose a Random Forest classifier model, as it tend to be relatively not too affected by outliers. After turning quality scores into three quality classes (poor, average and good) I fitted the model. Here is the classification report: <br>
![model classification report](https://miro.medium.com/max/846/1*tG1zSDgU-uAoTo8qjUVS-w.png)<br>

That report clearly shows that the unbalance between classes (a lot of average wines for few good ones and very few poor ones) is hurting the model. Ways to improve the accuracy score would be to hyper tune parameters with the existing classifier, try other classifiers to compare their accuracy and treat the outliers.


## Technologies Used
Python 3.9.7

## Setup
To run the project code on your local machine just follow these steps:

1. Clone the repository. 
   `git clone https://github.com/github_username/repo_name.git`
   
2. Open the jupyter notebook named Wine quality analysis.ipynb and run the cells.

The bolg post provides explantations on my thinking and why I am running all the different steps.

## Acknowledgements
Credits for the dataset belong to:
P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis.
Modeling wine preferences by data mining from physicochemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.

## Contact
Created by Julien Flandre  - feel free to contact me at julien.flandre@gmail.com!
