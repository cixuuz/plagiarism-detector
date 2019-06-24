# Plagiarism Detector
A plagiarism detector that examines a text file and performs binary classification; labeling that file as either plagiarized or not, depending on how similar that text file is to a provided source text.

# Runtime requirement
The notebooks need Python 3 environment. 

# Features Definition
One of the ways we might go about detecting plagiarism, is by computing similarity features that measure how similar a given text file is as compared to an original source text. Since our approach is based on this [paper](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/January/5c412841_developing-a-corpus-of-plagiarised-short-answers/developing-a-corpus-of-plagiarised-short-answers.pdf), we will create features called containment and longest common subsequence.  
1. Containment: first look at a whole body of text (and count up the occurrences of words in several text files) and then compare a submitted and source text, relative to the traits of the whole body of text.
2. Longest Common Subsequence (LCS): the longest subsequence common to all sequences in a set of sequences (often just two sequences).

# File Description
`2_Plagiarism_Feature_Engineering.ipynb` is about feature creation and datasets preparation.  
`3_Training_a_Model.ipynb` is to train the deep learning model.  
`source_pytorch` folder contains functions to train model and predict results.  

# Result
The trained model has 96% accuracy with 1 false positive and 0 false negative. 

|acutals\Predictions | 0 | 1| 
| --- |---|---|
|0| 9 | 1| 
|1| 0 | 15|

# License
The content of this repository is licensed under a [MIT license](LICENSE)
