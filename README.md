![image](https://sswm.info/sites/default/files/inline-images/WATER%20CHARITY%20n.y.%20Deep-well%20hand%20piston%20pump%20including%20apron%20and%20drain%20in%20Gambia.jpg)
# Water Pump Functionality Analysis In Tanzania

## Business Problem
Using data from the Tanzanian Ministry of Water, our goal is to predict if water pumps are functional or non-functional.

## Data
We have ~59,400 data from DataDriven. <br>
Our target class (functional and non functional) has a ~60/~40 split. <br>

## Preparation
We dropped duplicate features and unnecessary features for our model. We also replaced null object values to 'Unknown'.<br>

## Model Selection
We used DummyClassifier, Logistic Regression, KNN, RandomForestClassifier, and XGBoost models to find the best accurate predictions.<br>

## Results
The best model was XGBoost model with hyperparameter of 'model__max_depth': 7, 'model__n_estimators': 200. This model predicted accuracy of ~85.8%.<br>
![image](https://raw.githubusercontent.com/ericdnbn/phase_3_project/main/images/Confusion%20Matrix.png)<br>
The XGBoost model predicts 12,743 water pumps in the testing data correctly. The model also predicts 1,458 water pumps as non-functional when they are functional and it preditcs 649 water pumps as functional when they are non-functional.

## Feature Importance
With our best model, we checked which features were most impactful in our model.<br>
![image](https://raw.githubusercontent.com/ericdnbn/phase_3_project/main/images/Feature%20Importance.png)<br>
We found that the feature quantity_dry had the biggest impact, ~28.2%, and waterpoint_type_other had the second biggest impact on the model, ~12.4%.

## Conclusion
Our final model, XGBoost, gave us ~85.8% accuracy of predicting the functionality of the water pump.<br><br>
Given those features that have the greatest impact on the functionality of water wells in Tanzania our recommendations to the Tanzanian Ministry of Water are:
* Perform regular checks on the quantity of water in the wells, and take preventative measures to decrease the chances of them being non-functional.
* Replace waterpoint types with the designation of ‘other’ with more effective and widespread types, like gravity waterpoints.
* Put policies in place that ensure the company managing a well are performing regular checks and maintenance. Screen companies seeking to construct a well using a rigorous standard to decide if their project may go forward.

## Future Steps
Identify the categories of certain features that are labeled as ‘other’ and ‘unknown’. This will create more clarity and specificity within the dataset, and theoretically, a model that can make even more accurate predictions.
Use machine learning to create a model that predicts the quantity of water in a well, dry or not, to help the Tanzanian Ministry of Water be more proactive in performing checks and maintenance.

## Repository Structure 
```
├── Working_Notebook
│   ├── Eric's Notebook.ipynb     
│   ├── Mitch_Wkbook.ipynb     
│   ├── Soo's Work.ipynb    
│   └── Soohyun's work.ipynb
├── data  
│   ├── Col_Descriptions.docx
│   ├── Test Set Values.csv
│   ├── Training Set Labels.csv
│   └── Training Set Values.csv
├── images  
├── .gitignore
├── Final Notebook.ipynb
├── Powerpoint_Tanzanian_Water_Pump.pdf
├── README.md
```
