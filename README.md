#Analyzing COVID-19 Dataset

Notebooks for pre-processing and loading thousands of [CORD-19 scientific articles](https://allenai.org/data/cord-19) for automatic classification. These articles contain research on COVID-19 or related coronaviruses.
Initial pre-processing script borrowed from [Kaggle kernel by Maskim Ekin](https://www.kaggle.com/maksimeren/covid-19-literature-clustering/notebook), then heavily modified.

The general approach has been:

1. Provision an n1-standard-8 (8 vCPUs, 30 GB memory) VM Instance in Google Cloud. Use Deep Learning VM image to create it and make sure there's at least 500 Gb storage readily accessible to the notebook to save processed text files (those get massive!)
2. LoadData notebook contains code for parsing the files from the CORD-19 dataset, standardizing them somewhat by removing special characters, then transforming them into a dataset with single paragraph of text being used as a classification unit.
3. The training data was labeled manually (i.e., I read the articles and selected what I thought was an appropriate category from dropdown). I lack formal medical education (CompSci and Accounting degrees only), so my classification may or may not be correct.
4. I have no idea how well this classification will generalize to the wide corpus of data. That's the subject of exploration over the next month.

