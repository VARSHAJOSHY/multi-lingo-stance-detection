# multilingual-stance-detection

Stance Detection (SD) is the task of automatically determining whether the author of a text is for, against, or neutral towards a given target. Due to a lack of annotated data in other languages, the majority of stance detection research has focused on English. In this thesis, I investigate the difficulty of text encoding in the case of multilingual stance detection and compares the performance of traditional classifier models such as SVM and LR over BERT, as well as Multilingual Language Models (MLLMs) such as M-BERT, XLM, and XLM-RoBERTa when trained and tested in a multilingual setting. I also show how language imbalance and label(stance) imbalance contribute to the difficulty of the SD task. Annotated dataset used for this experiment contains tweets on various political debates in five different languages: English, Spanish, Catalan, French, and Italian. Extensive experiments show that MLLMs outperform both conventional classifiers and language-specific state-of-the-art transformer models. 

## Datasets
I chose existing benchmark datasets centered on four different political debates in five different languages for investigation: English, Spanish, Catalan, French, and Italian.

* E-USA - created for SemEval-2016 Task 6; 
* E-CAT - created for MultiStanceCat at Ibereval 2018 
* E-FRA - created by Lai et al., 2020 
* R-ITA - created by Lai et al., 2020

The datasets E-USA and E-FRA are about elections, whereas R-CAT and R-ITA are about referendums.

All four datasets have been annotated using the same guidelines proposed in Mohammad et. al.[2] for the English dataset. 
1.	FAVOR: The tweeter's support for the target can be deduced from the tweet.
2.	AGAINST: From the tweet, a reader can deduce that the tweeter is opposed to the target.
3.	NONE/NEUTRAL: A reader can infer from the tweet that the tweeter has a neutral stance on the target, or there is no clue in the tweet to reveal the tweeter's stance on the target (support/against/ neutral).

## Model
###	Baseline Models

* SVM with TF-IDF Vectorizer 
* LR with TF-IDF Vectorizer 
* SVM with Multilingual Universal Sentence Encoder (MUSE
* LR with Multilingual Universal Sentence Encoder (MUSE) 
* BERT

###	Multilingual Language Models (MLLMs)
* M-BERT 
* XLM 
* XLM-RoBERTa 

## Software and Tools

* SVM, LR, TF-IDF vectorizer  implementation in Python's Scikit-Learn library
* Huggingface pretrained BERT, M-BERT, XLM, XLM-RoBERTa (pre-cased version) used to fine tune on dataset
* Multilingual Universal Sentence Encoder from tensorflow-hub
* Visualization libraries – Matplotlib and Seaborn

## Setup

* Download the folders in Colab/Colab Pro
* Run main.ipynb file (make necessary changes according to your requirement)
* Run balanced_label.ipynb for uniformly distributing labels/stances across training set
* Run balanced_lang.ipynb for uniformly distributing languages across training set


