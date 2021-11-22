# Description of Contents

This repository holds code used in creating the practitioner guides published on the ADA website ([link](https://provost.uoregon.edu/ada/practitioner-guides)). The code regarding topic modeling (LDA), relevant words (TF-IDF), and preprocessing is in place. Additionally, a forthcoming methods paper at https://provost.uoregon.edu/ada/practitioner-guides/methods will help to provide context for the contents of the code stored here.

# Usage

You will want to start by vising the "how-to" folder. As directed by those documents, you may need to do some reading of official documentation for tools like conda or jupyter notebooks if you are new to data science in Python. In general, the only particularly complicated part (programming-wise) of this repository is using the LDA Job manager, so we recommend trying everything else out first. 

At the moment, each notebook is documented in its markdown, and some additional documentation is given in the how-to folder. If you are eager to use the code and can't find a solution with google, I recommend contacting analytics@uoregon.edu. Currently we are almost finished moving from our internal repository to this public repository.

For the most part, you will have to change file paths, tell the notebook which column in your data holds the text, and which holds the unique document index. All other options, such as parameter space and storage settings, can (and should be) changed, but do not necessarily need to be changed for the notebooks to run.

# Other Details

All computation in this project was done on compute instances in Microsoft Azure's Machine Learning resources. Depending on the size of your textual dataset and how thorough you want to be, you might also want to use external computing resources. 
