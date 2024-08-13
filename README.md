# Bankruptcy-Prediction
This project aims to improve the accuracy of predicting company bankruptcy using financial ratios and data from the Taiwan Economic Journal (1999-2009). Accurate predictions are crucial for protecting investments, minimizing financial risks, and ensuring the stability of the financial system.

## Methodology 

The dataset, containing 95 financial ratios, was first read into a pandas dataframe, and then cleaned to ensure all values were numerical. I explored the data using visualization tools and found that 220 out of 6,819 companies went bankrupt. To simplify the analysis, I identified the 15 most important features using the feature importance command from decision trees.

I experimented with multiple machine learning algorithms, including K-Nearest Neighbors, Random Forests, Logistic Regression, and Linear Regression. For logistic regression, the data was split into training and testing sets, scaled the features, and used the model to predict bankruptcy. The model was tested using financial ratios from Alphabet Inc. and Enron. Similarly, I applied multiple regression without scaling the data but adjusted probabilities to fit within the 0-1 range.

To ensure accuracy, I fine-tuned the parameters of each algorithm, such as n_neighbors, n_estimators, and max_depth, and adjusted the test size for logistic regression. This comprehensive approach allowed me to assess the effectiveness of various models in predicting bankruptcy.

## Results

The analysis demonstrated that K-Nearest Neighbors and Random Forests performed exceptionally well in predicting bankruptcy, with scores of 0.966 and 0.970, respectively, even after parameter adjustments. Logistic regression also proved highly accurate, predicting a near-zero probability of bankruptcy for Alphabet Inc. and a near-certain probability for Enron. Multiple regression yielded similar results, accurately reflecting the actual outcomes. The classification report further validated our model’s effectiveness, showing a precision of 0.97, recall of 1.00, and an F1-score of 0.98. Overall, the models demonstrated strong predictive capabilities in assessing bankruptcy risk.
