# DearWatson

This project may be found in kaggle.com competitions (https://www.kaggle.com/c/contradictory-my-dear-watson) where I needed to find the relationship of two sentences as being (entailment, contradiction, or unrelated). The sentences were mostly in English but several otehr languages were used as well. I used a total of three models for this project. A SVM, Random Forest, and BERT. The first two models had about a 37-39% accuracy while the BERT (our best model) attained a 67% accuracy. 

The two sentences (premise, hypothesis) were joined using a [SEP] separator which represents one X datapoint, and a label y of 0,1,2 (entailment, contradiction, or unrelated, respectively). A [CLS] tag was added at the beginning of each sentence for tokenization in preparation for feeding into BERT model.

BERT (BiDirectional Encoder Representations from Transformers) is a model that uses a neural network to classify the relationship as entailment, contradiction, or unrelated. BERT utilizes vectorized, numerical representations (called embeddings) but also studies the context of the word as its relation within the sentence to give a much more accurate representation of the word (transformers). BERT is a state of the art transfer learning model that can be used to predict next sentences. 

Random Forest Model had parameters 2000 estimators, 6 max_splits, 2 min child weight, entropy. SVM model had a poly kernel, C=.01. Both models had approximately 37% accuracy. LGBM model with Voting classifier would be next attempt at stengthening model. Alos looking into class imbalance may help to boost accuracy of model.
