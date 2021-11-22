# Using LDA Job Manager

If you want to recreate the entire process we used to make the practitioner guides, you will need to go through the LDA Job Manager or make your own equivalent process.

## Experiment Files

The first quirk of the LDA Job Manager is that it can take (and expects by default) settings via a .json file. This behaviour can be overidden by uncommenting commented code in the notebook itself. The idea of "experiments" as the notebook calls them is that a general list of settings (such as data path or stop words) might be defined at top notebook level, and then each experiment as listed in the .json file provides extra settings and/or a set of settings overrides, for example to try out different fitting methods, or to look at different subsets of the data. Ultimately the purpose of the LDA Job Manager is to manage settings and file management. For each settings specification, it will create a folder, put those settings in a .json file, put a gridsearch notebook into that folder, and tell the gridsearch notebook to run.

## Run Settings

For the most part, settings should either be self-explanatory, or explained in the Gensim documentation for LDA. Two that bear mentioning are "filter_column" and "acceptable_values." The LDA job manager is not actually designed to look at an entire textual dataset, but to look a subsets of the data where values in "filter_column" are in the list "acceptable_values." An easy to get around this is to add a dummy column to your data. Editing the gridsearch and LDA job manager notebook for your specific purpose also shouldn't be too hard if you have experience with Python.

## Gridsearch

The default behavior of the gridsearch notebook is to look a topic models fit for differing numbers of topics. It can be edited to do a more traditional gridsearch over other hyperparamter options, although we did not find that to be necessary for our application. The main information of interest in the gridsearch notebook is the graph of coherence score versus topic number near the bottom (there's a link) which is helpful in choosing which topic models to inspect by hand.

## Explorer

After running the gridsearch, you will want to run the explorer notebook that you find in each run folder. Those notebooks have minimal dependencies, and can be run in a base conda environment, and so can be easily shared with others as long as they have the textual data.