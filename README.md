#### phase-3-project

# Why this data?
Rainbow Six Seige (R6S) is a highly competitive first person shooter game developed by Ubisoft. the game pits teams of five players each against each other in alternating rounds where the team that completes the objective, or eliminates the oposing team, wins.
the game has become very competitive in it's lifespan and has professional competitions where hundreds of thousands of dollars are offered as prize money
the game has a ranking system to ensure players are matched fairly against each other. the higher ranking players, are also considered for professional competition

For newer players, getting more wins is essential to growing in rank

### awareness of old data
the dataset used in this project was from season five in 2018. four years have passed and several updates to the game have hence taken place, rendering the data itself moot
however, i am fairly confident that the methods used in modelling and classifying would still predict features that lead to winning a match

# in this repository
1) uploadable_data
    this is a folder with a csv file containing a small fraction of the incredibly large data set that i used. the uploadable data is for viewing, and running the notebook quickly. to get the FULL, but incredibly slow processing verion of the 20gb (yes, gigabyte) data, download it here <a>https://www.kaggle.com/datasets/maxcobra/rainbow-six-siege-s5-ranked-dataset</a>

2) index.ipynb
    a jupyter notebook exploring what features of a match, and player, might be classified to lead to a win

3) xxx_xxx.pkl 
    several pickle files of models that i created, to help someone re-running the index file to get results faster. the models, if run without the pickle files, can be expected to take 20-30 minutes MINIMUM to process

# Researching R6S data
the data had a column `haswon` that i used as the target variable. all other variables were either arbitrary (`match_id` and similar), direclty correleated, due to being outcomes of the target (`rank` an similar) or were categorical. i removed anything non categorical.

i also removed any row that didn't have the `game_mode` as `BOMB` being that bomb mode is what's used in professional competition.

# Making Models
i used 3 models. DecisionTreeClassifier, KNearestNeighbors, RandomForestClassifier. being that the target was boolean and all the features are categorical

# Assesing Models
i used several methods to asses the models, but paid attaention to F1 score mostly. i also was looking for a model that precision was given more weight

feel free to comment and correct this notebook, all criticism is welcome