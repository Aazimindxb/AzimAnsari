<a> <img src="https://github.com/Aazimindxb/AzimAnsari/blob/main/GCP-Data-Engineering-Projects/Project-Titanic/titatic_shipwrecks.png" alt="Titanic Shipwreck" width="860" height="250">
</a>

# 01 Project Titanic
This project is based on the legendary Titanic ML competition, which serves as an excellent starting point for diving into machine learning competitions and getting familiar with the Kaggle platform. The competition’s objective is straightforward: use machine learning to create a model that predicts which passengers survived the Titanic shipwreck. The sinking of the Titanic on April 15, 1912, during its maiden voyage, is one of the most infamous shipwrecks in history. With only a limited number of lifeboats available, 1502 out of 2224 passengers and crew lost their lives. This challenge involves building a predictive model to answer the question: “What sorts of people were more likely to survive?” using passenger data such as name, age, gender, and socio-economic class. For more details and to join the competition, visit the Kaggle platform and check out Alexis Cook’s Titanic Tutorial for a step-by-step guide on making your first submission.


## Overview

Here you want to write a short overview of the goals of your project and how it works at a high level.

Key phases of machine learning ML project:
1. Load data in BigQuery
2. Select and preprocess Features
3. Create the Model inside BigQuery
4. Evaluate the performance of trained model
5. Use the model to make predictions

## Architecture

Here you want to write a short overview of the goals of your project and how it works at a high level.

## Environment

Programming Language: Python
Structured Language: SQL
Google Cloud Platform:
    - BigQuery
    - Cloud Storage
    - Looker Studio
    - Compute Instance

## Dataset

Here you want to write a short overview of Dataset. How this dataset can be used in this project.

## Schema

Here you want to write a short overview of Dataset. How this dataset can be used in this project.

## Project Files (Scripts)

Some basic commands we have used in this project:

Create a dataset in BigQuery:
```
```

###Create a ML model in BigQuery:
```
CREATE OR REPLACE MODEL 'project_titanic.pt_model'
OPTIONS(model_type='logistic_reg',
        input_label_cols=['Survived']) AS
SELECT * FROM 'project_titanic.training_data' ;
```

###Evaluate the model in BigQuery:
```
SELECT * FROM ML.EVALUATE(MODEL 'project_titanic.pt_model') ;
```

###Use model for prediction in BigQuery:
```
SELECT PassengerId,predicted_Survived
FROM
ML.PREDICT(MODEL 'project_titanic.pt_model',(
SELECT * FROM 'project_titanic.testing_data'))
ORDER BY PassengerId ;
```

## How to run

Here you want to write a short overview of Dataset. How this dataset can be used in this project.

## Lessons Learned

It's good to reflect on what you learned throughout the process of building this project.

## Reference

Here you want to write a short overview of Dataset. How this dataset can be used in this project.


## [Presentation with Looker](https://lookerstudio.google.com/reporting/92dfa589-74ce-426c-8807-c12c39b5e152)



## Contact

Please feel free to contact me if you have any questions at: <a href="https://ae.linkedin.com/in/aazim-ansari">
    <img src="https://github.com/Aazimindxb/AzimAnsari/blob/main/GCP-Data-Engineering-Projects/LinkedIn_Logo.png" alt="LinkedIn" width="60">
</a>

