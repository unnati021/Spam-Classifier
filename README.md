# Spam-Classifier
Under Spam Classifier, we will be training a classifier to classify whether a given email, x, is
spam (y = 1) or non-spam (y = 0). SVMs will be used to build the spam filter .

The script ex6 spam.m is used to build a spam classifier , which calls multiple scripts needed to build the classifier.

In processEmail.m, we have implemented the email preprocessing and normalization steps like lower casing , striping html , normalizing urls , word stemmimg .

After preprocessing the emails, we have a list of words for
each email. The next step is to choose which words we would like to use in
our classifier and which we would want to leave out . 

The complete vocabulary list is in the file
vocab.txt . Our vocabulary list was selected
by choosing all words which occur at least a 100 times in the spam corpus

Given the vocabulary list, we can now map each word in the preprocessed
emails into a list of word indices that contains the index
of the word in the vocabulary list .

We will now implement the feature extraction that converts each email into
a vector .  emailFeatures.m feature vector for an email, given the word indices.

After the feature extraction functions, the next step of
ex6 spam.m will load a preprocessed training dataset that will be used to train
a SVM classifier. spamTrain.mat contains 4000 training examples of spam
and non-spam email, while spamTest.mat contains 1000 test examples. Each
original email was processed using the processEmail and emailFeatures
functions and converted into a vector x.

After loading the dataset, ex6 spam.m will proceed to train a SVM to
classify between spam (y = 1) and non-spam (y = 0) emails
