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
At the end of this project, two main iterations on a churn-prediction model were implemented and evaluated. The first model used a simple pivot of the event containing the most relevant difference between churning and non-churning users.
Three models are trained with this data, given the following F1 Values:
Gradient Boosted Trees - 68.9%
Random Forest - 68.4%
SVM - 68.4%

While the values look promising, an inspection of the confusion matrices revealed that SVM and Random Forest classified all users as non-churning. However, because of the relatively low number of churned users, the F1 score was still reasonably high.

The best performing model for the first iteration was Gradient Boosted Trees, which managed to predict 17 churners correctly.

Two new features are introduced for the second iteration—the number of sessions and days from first to last recorded event.

Gradient Boosted Trees algorithm trained again using these features.

The results were much better than the initial attempt. With an F1-score of 89.1% for validation data, and 294 correctly identified churners, the second iteration of the model is a great first model which could be fine-tuned and improved even more.

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
The results of the blog will be found [here] (https://medium.com/@hessa.shamnad/churn-up-with-sparkify-78369f1c6d6f)
