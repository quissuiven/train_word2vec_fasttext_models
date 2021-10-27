# Training Word2Vec and FastText word vector models for non-English languages

This repo is modified from [this great project](https://github.com/Kyubyong/wordvectors). Credits to Kyubyong!

Given that it's been a while since Kyubyong's project was updated (Sep 2017), some of the codes weren't working. Thus, I have refactored the code to work for Python 3, as well as the latest versions of Gensim.

We can use this code to train our own Word2Vec or FastText word vector models for non-English languages.

## Requirements
* nltk >= 1.11.1
* regex >= 2016.6.24
* lxml >= 3.3.3
* numpy >= 1.11.2
* konlpy >= 0.4.4 (Only for Korean)
* mecab (Only for Japanese)
* pythai >= 0.1.3 (Only for Thai)
* pyvi >= 0.0.7.2 (Only for Vietnamese)
* jieba >= 0.38 (Only for Chinese)
* gensim > =0.13.1 (for Word2Vec)


## Work Flow
* STEP 1. Download and unzip [wikipedia database backup dumps](https://dumps.wikimedia.org/backup-index.html) of the language you want.
  - For example, for Indonesian, we will search for "idwiki" and download the [file for "Articles, templates, media/file descriptions etc"](idwiki-20211020-pages-articles-multistream.xml.bz2)
* STEP 2. Copy the xml file to `data/` folder.
* STEP 3. Run `build_corpus.py`.
* STEP 4. Run `make_wordvector.py` to get Word2Vec or FastText word vectors.
