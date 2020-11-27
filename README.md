# What do Australians think of Buying Now & Paying Later? A Sentiment Analysis of Australia's BNPL Service Providers Based on User Reviews.

## Introduction
This project uses NLP to predict the sentiment of user reviews. More specifically, reviews of users utilising BNPL services (such as Zip Pay, Afterpay, Klarna, Sezzle). 

Through this project, we’re looking to gain insights on what users like/dislike about the service, what current issues are they facing right now and what are our competitors doing that we could implement or improve upon.

Answering these questions will help us understand what can be changed about our product, it’ll help us deal with pressing issues as soon as they occur and will help us gain an edge over our competition.


## The Data
Since the BNPL sector is still very recent, there isn’t a lot of publicly available datasets. In order to get my hands on the dataset used, I had to ethically scrape (not for commercial use) text reviews off a product review website called Trustpilot. The reviews scraped were from Klarna and Sezzle. Because both aren’t Australian companies, I wanted to see how users perceive them here (in Australia).


## The Method
After extensive text cleaning, making it ready for use (lemmatisation, tokenisation) and some EDA, I deployed ML models (from Logistic Regression to Tree Based Algorythms like XGBoost) and DL models as well (LSTM, GRU).


## Results
Surprisingly, the ML learning models yielded the better accuracy with CV Logistic Regression taking the crown (94.6%).

But the Precision and Recall metrics tell a much different story. Going by the Precision and Recall scores, XGBoost yielded the best results (93.1% & 98.7% for the positive ratings category).

Moreover, the DL models tell a completelly different story with accuracy scores coming in below 1% consistently.



## Learnings
So why is it that the ML models and the DL models yielded such different results?

Because the data collected was highly skewed. 80% of reviews were positive, almost 20% were negative while less than 1% were neutral. This explains why the accuracy and precision, recall scores were so different in the ML models. This also explains why the DL models performed so poorly on the testing set, the text given to the models was overwhelmingly classified as positive.



### Thank you for reading this, I hope you enjoy this project as much as I enjoyed working on it.
