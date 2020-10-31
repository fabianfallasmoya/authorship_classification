This is just a backup repo. See the original repo at:
https://github.com/edponce/DoyleInvestigators2/edit/main/README.md

## General Information

The `authordetect` package follows a modular object-oriented approach.
The most relevant classes are:
* `Author` (*authordetect/author.py*) - This class represents a corpus
  corresponding to a single author and provides capabilities to load and
  tokenize corpus, partition into documents, create embedding models for author
  and each document. All these actions are part of the `writer2vec` algorithm
  (see Overleaf paper), and a method with the same name is provided that
  applies these transformations as a single step.
* `Tokenizer` (*authordetect/tokenizer.py*) - This class represents a tokenizer
  for performing sentence segmentation and tokenization of an `Author's`
  corpus. It also contains a list of stopwords (from NLTK).
* `Classifier` (*authordetect/classifier*) - This class represents a MLP
  classifier and is used to train on document vectors (with corresponding
  lables). Afterwards, it can provide predictions on new document vectors.
