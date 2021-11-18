# Description of Contents

This repository holds code used in creating the practitioner guides published on the ADA website ([link](https://provost.uoregon.edu/ada/practitioner-guides)). Right now the code regarding topic modeling (LDA), relevant words (TF-IDF), and preprocessing is in place, while additional tutorials and a simplified topic modeling notebook will be added soon. Additionally a forthcoming methods paper at https://provost.uoregon.edu/ada/practitioner-guides/methods will help to provide context for the contains of the code stored here.

# Usage

You will want to start by setting up a conda environment for the project. You can import the file stored in the "Environments" folder, which contains the actual environment used, or you can set up a base conda environment and add Gensim and Spacy (There aren't many dependencies). 

At the moment, each notebook is documented in its markdown, and full documentation is forthcoming. If you are eager to use the code, I recommend contacting analytics@uoregon.edu. Currently we are working on moving from our internal repository to this public repository.

For the most part, you will have to change file paths, tell the notebook which column in your data holds the text, and which holds the unique document index. All other options, such as parameter space and storage settings, can (and should be) changed, but do not necessarily need to be changed for the notebooks to run.

# Other Details

All computation in this project was done on compute instances in Microsoft Azure's Machine Learning resources. Depending on the size of your textual dataset and how thorough you want to be, you might also want to use external computing resources. 
