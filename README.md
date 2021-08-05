# Sparkify
## Project Definition
### Overview
This is the final project from the Data Science  Nanodegree course, and in this, we will create a machine learning model, which will predict when users at Sparkify are about to churn.

The possible event types are:
•	Cancel
•	 Submit Downgrade
•	 Thumbs Down
•	 Home
•	 Downgrade
•	 Roll Advert
•	 Logout
•	 Save Settings
•	 Cancellation Confirmation
•	 About
•	 Settings
•	 Add to Playlist
•	 Add Friend
•	 NextSong
•	 Thumbs Up
•	 Help
•	 Upgrade
•	 Error
•	 Submit Upgrade

Where the type 'Cancellation Confirmation' is considered as users churning.


### Problem
The problem statement of this project is to predict the churn. Predicting user churn rate is one of the most challenging and everyday tasks in any customer-oriented business. If such problems are correctly explored and analyzed by data scientists and analysts, data science techniques can assist with various algorithms to solve them.


### Expected Results
At the end of this project, a model for churn prediction should be created and evaluated. The model should have been trained and tested on a subset of the 12GB of data, and the final testing should happen on the utterly separate validation set. An accuracy F1-Score confusion matrix uses to evaluate the performance and feasibility of the model.


### Actual Results
After data exploration and understanding what features relate to user churn, we built multiple models using different methods to predict users who will churn. 3 different classifiers were used :

Random forest classifier
Gradient boosted tree classifier
Logistic regression

For each of the above a baseline model was built using the default hyper parameters and then used 3-fold cross validation to fine tune the hyper parameters

The best model was chosen on the basis of F1 Score that gives equal importance to precision and recall. The model that performed the best was the tuned Random Forest classifier .

## Overview of Files
### Data Files

README.md

Sparkify.ipynb - notebook used for POC in Udacity Workspace

mini_sparkify_event_data.json - starting data file containing the streaming music provider's user logs

## Improvement
To achieve the optimal user experience, using more capable hardware and moving the text extraction process from the cloud to the device would be essential. This would reduce the processing time and give access to the outputs of all of the modules of the text extraction pipeline, which would, in turn, enable the following features:

•	 User-guided reading (e.g., read the big text first, or read the text the user is pointing at)
•	 Better support for languages other than English
•	 Output filtering (e.g., ignore text smaller than some adjustable threshold)
•	 Passive text detection (auditory cue on text detection, perhaps with additional information encoded in the tone and volume)

The user experience could also be improved significantly by using MXNet, a deep learning library that is better optimized for mobile devices than TensorFlow. The speedup would not be enough for running text extraction on the device, but it would reduce the classification delay significantly.


## Results
The results of the blog will be found (https://medium.com/@hessa.shamnad/churn-up-with-sparkify-78369f1c6d6f)
