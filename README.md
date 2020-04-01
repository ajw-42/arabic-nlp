# arabic-nlp
This repo explores the value of several common text classification techniques for an Arabic language dataset. It also serves as an introduction to those techniques for a reader who has basic or intermediate Python skills but little familiarity with machine learning and text classification.

Each notebook also digs into the data to offer some thoughts on what types of text provide a challenge for each text classification approach. **But you don't need to understand any Arabic to (hopefully) benefit from the explanations of machine learning and text classification!**

We use this dataset of Arabic news labeled for category: https://data.mendeley.com/datasets/322pzsdxwy/1

The authors provide this description of the dataset:
>RTAnews dataset is a collections of multi-label Arabic texts, collected form Russia Today in Arabic news portal. It consists of 23,837 texts (news articles) distributed over 40 categories, and divided into 15,001 texts for the training and 8,836 texts for the test. The original dataset (without preprocessing), a preprocessed version of the dataset, versions of the dataset in MEKA and Mulan formats, single-label version, and WEAK version all are available.

`0-text-preprocessing.ipynb` cleans the raw dataset and produces a train/val/test split that we'll use throughout this repo for consistency.

`02-sklearn-binary.ipynb` simplifies our problem to binary classification and introduces the text classification utilities in `sklearn`.

`03-sklearn-multiclass.ipynb`introduces the multiclass classification utilities in `sklearn`, since our dataset actually has 40 categories of news.

`04-word2vec.ipynb` introduces the concept of word embeddings and uses word2vec to train word embeddings from scratch with `gensim`.

`05-fasttext.ipynb` uses pre-trained embeddings for Arabic available through the `fasttext` package.

`06-laser.ipynb`introduces LASER, a single set of multilingual word embeddings.

`07-multilingual-bert.ipynb` introduces transformer models in general and multilingual BERT, a large language model pre-trained on many languages including Arabic.
