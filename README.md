# Skim_lit_pub_med
This project mainly focuses on sequential sentence classification of medical abstracts and is based on the paper published by Franck Dernoncourt and Je Young Lee
in 2017(https://arxiv.org/abs/1710.06071). We have used the pubmed 20k dataset for our sequence classification and have six different models for this classification.
The first model was a baseline model created by pipelining the tfidfVectorizer and Multinomial Naive Bayes layer.
Second model was a conv1D model which was fed with custom token embeddings as input.
This model was again followed by a model which used pretrained embedding layer from tensorflow hub namely , the universal sentence encoder.
Next we created a Conv1D model again but this time using character embeddings and evaluated it's results.
Our fifth model was a multi nodal model which took both token embeddings and character embeddings as input.
Finally, we used feature engineering to create positional embeddings and fed them into our final model along with the token and character embeddings.
We have also used tensorflow.data API in order to create fast input data throughout this project(specially in the last two models where we are using multi nodal inputs).
In the end we have compared the results of all our models(accuracy, precision,recall,f1_score) by creating a dataframe and graphically plotting it.We have also saved our best performing model.
