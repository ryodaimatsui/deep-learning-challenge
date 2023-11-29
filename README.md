# Deep-Learning-Challenge

## Overview of Analysis

In response to Alphabet Soup's objective of optimizing funding selection for success, this analysis involves utilizing deep learning models in order to generate a binary classifier. The dataset, comprising over 34,000 organizations that have received Alphabet Soup funding, contains key metadata columns such as APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, and IS_SUCCESSFUL. The goal is to develop a predictive model that classifies organizations based on their likelihood of success when funded by Alphabet Soup. This entails leveraging the provided features to train a binary classifier, enhancing the foundation's ability to make informed decisions in selecting applicants with the highest potential for success in their ventures.

## Results
### Data Preprocessing 
- For all three deep learning models — contained in, AlphabetSoupCharity.ipynb, AlphabetSoupCharity_Optimization.ipynb, and AlphabetSoupCharity_Tuning.ipynb — the column titled, "IS_SUCCESSFUL," served as the target variable. The variable contained information regarding the success or failure of past organizations encoded in either 1 or 0, respectively.
- As for the features, all three deep learning models utilized the columns, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT. In order to be used in the models, however, the columns were transformed from categorical data to numerical data. Moreover, the large number of categories contained within certain columns necessitated the generation of an "Other" category for categorical reduction.
- Lastly, the columns "EIN" and "NAME" were removed from the input data for all three models as they were neither targets nor features.
<img width="1395" alt="Screenshot 2023-11-29 at 11 58 25" src="https://github.com/ryodaimatsui/deep-learning-challenge/assets/137141385/42d23953-d373-47f4-8f7c-0c6b250a2e9d">

### Compile, Training, and Evaluating the Model
- For the initial model, two hidden layers were created with 80 and 30 neurons respectively. Both layers utilized the "rectified linear unit" activation function.
<img width="494" alt="Screenshot 2023-11-29 at 11 51 20" src="https://github.com/ryodaimatsui/deep-learning-challenge/assets/137141385/2621739e-17af-4a48-a995-c2cd6475faeb">

- In contrast, the second model designed for optimization utilized the same hyperparameters with the addition of one additional hidden layer with 30 neurons and the same activation function.
<img width="494" alt="Screenshot 2023-11-29 at 11 51 20" src="https://github.com/ryodaimatsui/deep-learning-challenge/assets/137141385/443a712b-d058-41a8-a085-73575c64bb37">

- For the third model, a function was created to identify the optimal hyperparameters.
<img width="801" alt="Screenshot 2023-11-29 at 11 53 43" src="https://github.com/ryodaimatsui/deep-learning-challenge/assets/137141385/08a3a3f1-8692-4f54-b411-92f2486b1d87">

- While such steps were taken in order to increase the target performance of over 75%, all three models failed to do so, reaching only 72% accuracy.

### Summary
- While the models failed to achieve the target performance higher than 75% accuracy, they may still aid in the decision for funding organizations. In other words, although it is preferable to have models that perform at an accuracy of 90% or higher, the models are able to accurately predict the success of roughly 7/10 organizations. In future models, it would be perhaps best to coordinate with a funding specialist or director to identify ways in which the features, and thus, categorical data, can be reduced. Additionally, it would benefit the deep learning models to collect more data for training. 








