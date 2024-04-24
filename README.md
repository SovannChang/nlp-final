# nlp-final
** A NOTE: THE DATA IS TOO LARGE TO BE UPLOADED TO GITHUB. IT CAN BE DOWNLOADED FROM https://www.kaggle.com/datasets/meruvulikith/190k-spam-ham-email-dataset-for-classification**

This repository stores the code and research paper for my Vanderbilt 5780 Natural Language Processing final project. The goal of this final project is to investigate the effectiveness of a logistic regression model trained only on Term frequency-inverse document frequency data. A second goal was to determine whether including the rate of misspelled or otherwise invalid words in an email could provide a noticeable (2% or greater) increase in the model’s performance.

The data used for this analysis was retrieved from Kaggle using the above link. It contains around 190,000 samples of email text, each labelled as ham or spam. Because of limited compute and time, the dataset was randomly reduced to 20,000 rows. The 20,000 rows of data were cleaned, transformed using scikitlearn's TfIdfVectorizer, and split into training and testing sets. The resulting feature matrix is used to train a scikitlearn LogisticRegression model, which was used as evidence to answer the question posed in the first goal of the project.

In addition to the first model, a second model is trained using the original feature matrix with one column added, representing the percentage of invalid words in each email. The performance of this second model is compared to the first model, providing evidence to answer the question posed in the second goal of the project.
