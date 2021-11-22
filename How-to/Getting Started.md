# Getting Started

## Code Tools

If you haven't already, you will first want to import the required libraries and download a code editor suitable for notebooks. See the "Using Conda and Jupyter" how-to for help on that.

## Analyzing Text

In general, each notebook will contain instructions on what it needs and how it is used. 

### Data

You will need a dataset (default .csv format) with a column of text entries and a columns of document-level ID's. These can be numbers 1-infinity, strings etc, they just need to be unique. You can easily use the Pandas library to added such an index column to your data if you don't keep track of your text in another way.

### Topic Modeling

A good place to start is in the "quick-lda" notebook. You will only need to edit the notebook with a few details about your data, such as column names, data location etc., then you can run the entire notebook. This notebook is intended to give the user a very brief non-rigourous decomposition of their textual dataset, and to give the user an idea of what kind of model inspection is involved in using LDA more thoroughly. LDA doesn't require good preprocessing to function, but you will find it easier to interpret results after using the preprocessing notebook on your text.

### Simple calculation of relevant words

The TF-IDF calculation is also a great place to start. It is much easier to interpret correctly than LDA results, but is ultimately much less rich results-wise. These calculations are valuable for when you have a particularly interesting subset of your textual dataset and you want to what words are uniquely relevant to that subset (in contrast to the whole textual dataset). The TF-IDF calculations are in general much more reliant on proper preprocessing, so it is recommended to use the preprocessing notebook first.

### Preprocessing

Using the preprocessing notebook is highly recommended. The main challenge in getting it to work is making sure you have the "en-core-sm" trained pipeline from Spacy installed correctly. The notebook shows how that can be done. The main feature of the preprocessing notebook is that it performs lemmatization, which is the process of converting words into their base or root forms. This process greatly reduces the set of words that text models and the humans interpreting them have to look at. LDA is fairly unique among text models in that preprocessing isn't really a requirement. In general, you should use the preprocessing notebook to create a new textual dataset and use that you all of your text analysis.

## Errors

Errors can be quite long when using notebooks, so make sure to scroll down the the bottom to get the short description. For the most part, errors will occur due to not setting up and connecting to the packges/environment correctly. Keep in mind that every part of each notebook can be inspected and edited.