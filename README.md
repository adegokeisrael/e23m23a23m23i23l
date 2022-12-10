
# A multi-modal based BERT-embedded system for spam filtering

The output dataset is an extention of the existing input dataset retrieved from the [SMS Spam Collection Dataset](https://www.kaggle.com/uciml/sms-spam-collection-dataset).

This repo stores the input dataset, the dataset with the embeddings and the code used to generate this dataset.
## Architecture
![Capture](https://user-images.githubusercontent.com/47308654/206814161-0e9e918f-ee51-4cf1-9b80-87bfe33e92da.PNG)
## This project implements a fully funtional flask interfaced app written majorly in python for spam filtering. It employs a multi modal blocks consisting of a BERT Model,Light GBM classifier and a Naive Bayes classifier. The project reads email messages via the google gmail API and run it through our classifier to evalute its content. The result of evaluation is the prensented on the front-end.
## modals employed
* Bidirectional Encoder Representations from Transformers (BERT) is a transformer-based machine learning technique for natural language processing (NLP) pre-training developed by Google. With Google leveraging BERT in its search engine,and across it text based product and by late 2020 it was using BERT in almost every English-language query. The model have been trained on extremely large corpus of text all over the web, hence having a good sense of text intent and 'understanding'.
* Light GBM(Gradient Boosting machine) Classifier
* Multinomial Naive Bayes


## Input Dataset Structure
The original dataset contains 5574 english messages each labelled as *spam* or *ham*
This dataset contains 4 columns:

- `v1` -> Target column specifying if the message is *spam* or *ham*
- `v2` -> The original unprocessed messages
- `Unnamed_col_1` & `Unnamed_col_2` -> Columns with mostly missing values (around 99%) that are discarded

## Encoded Dataset Structure

The output encoded dataset contains the same information as the input dataset plus the additional DiltilBERT classification embeddings. This results in a dataset with 770 columns:

- `spam` -> Target column specifying if the message is *spam* or *ham*
- `original_message` -> The original unprocessed messages
- `0` up to `768` -> columns containing the DistilBERT classification embeddings for the message, after it being processed

<h3>Libraries Used</h3>
1. Flask<br>
2. gunicorn<br>
3. itsdangerous<br>
4. Jinja2<br>
5. MarkupSafe<br>
6. Werkzeug<br>
7. Pillow<br>
8. Pickle<br>
9. NLTK<br>
10. Numpy<br>
11. Scikit-learn<br>
12. Pandas<br>
13. Seaborn<br>
14. Joblib<br>
15. Matplotlib<br>
16. HTML<br>
17. CSS<br>
18. Bootstrap<br>
19. JavaScript<hr>

<h3>Project Walkthrough</h3>
1. Exploratory Data Analysis(EDA)<br>
2. Data Cleaning<br>
3. Data Manipulation<br>
4. Feature Engineering<br>
5. Applied Stemming and Lemmatization techniques (Snowball Stemmer, Porter Stemmer, and Wordnet Lemmatizer)<br>
6. Implemented Bag of Words model on the dataset<br>
7. Implemented TF | IDF <br>
8. Model Building - Used Multinomial Naive Bayes and Light GBM Classifier.<br>
9. Exported Multinomial Naive Bayes Classifier model using Joblib library<br>
10. Implemented DistilBERT - a hugging face transformer model <br>
11. Fine Tuned DistilBERT<br>
12. Developed Front End <br>
13. Created a flask server and deployed the code<br>
14. Web-app working Heroku<hr>

## Procedure







Almeida, T.A., Gómez Hidalgo, J.M., Yamakami, A. Contributions to the Study of SMS Spam Filtering: New Collection and Results.  Proceedings of the 2011 ACM Symposium on Document Engineering (DOCENG'11), Mountain View, CA, USA, 2011

