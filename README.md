# ANSC-6040-Project-1
Project 1 for ANSC 6040 class. 

## Project objective:
Using the farm's historical parlor data to assign the most likely cow ID to the records with missing IDs, based on individual cow parlor performance. 

## Naming convention: 
The first letter of each word in the variable name will be capitalized with no space between words.  

## Project plan:
- Timeline:
  
    *Week 4 (9/14)*: setting up repository, import appropriate packages and load data, explore data structure and missing data
    
    *Week 5 (9/21)*: apply machine learning for problem solving. Specifically predicting cow IDs.

    - Data Cleaning:
 
          - Remove duplicate rows
          - Perform z-standardization on applicable variables (AvgMilkFlow, Flow30_60Session, YieldSession) to remove outliers (> 2 SDs)
          - Drop all rows where features contain missing values
    
    - Splitting dataset:
 
          - Test set: rows without cow ID
          - Training set: 80% of rows with cow ID (randomly selected)
          - Validation set: 20% of rows with cow ID (randomly selected)
   
    - Model training:
      
          - Supervised learning to predict cow IDs
      
            - K-Nearest Neighbors

    - Model testing
 
    - Model performance
      
          - Accuracy
 
    - **Outcome**: generating a model that would predict cow ID based on all variables presented and complete the cow ID column of the dataset.
    
    *Week 6 (9/28)*: apply machine learning for problem solving. Specifically for days in milk (DIM), reproductive status (RPRO), and lactation number (LACT).
  
    *For each outcome variable:*
  
    - Splitting dataset:
 
          - Test set: rows without DIM/RPRO/LACT
          - Training set: 80% of rows wihtout missing data (stratified sampling on reproduction status)
          - Validation set: 20% of rows wihtout missing data (stratified sampling on reproduction status)
   
    - Model training:
      
          - Supervised learning with Random Forest
      
    - Model testing
 
    - Model performance
      
          - Accuracy
 
    - **Outcome**: If rows from cows with the same ID are clustered, will the model be able to fill-in-the-gap for DIM/RPRO/LACT? 
    
    *Week 7 (10/5)*: project summary, troubleshooting, preparation for poster presenetation.
  
- Methods:
    VS code will be used. Changes will be made locally then pushed to the cloud. 

# Project Summary
A Random Forest model was trained based on a subset of 448 cows, and the model's top-1 accuracy was 3.6%. 

The same model was applied to the real-world data with missing cow IDs, and the resulted accuracy was 0% (0 out of 1.7M records were predicted correctly). This model is thus completely unsuitable for predicting cow IDs for this farm, and it is farm from being industry ready. 

Pitfalls of this model are many. It was limited and only trained on a subset of cows, which was not representative of the whole herd. The Random Forest algorithm does not suit the purpose of this project well, as there were over 9000 different cows to predict upon. Event date also can provide critical information on model training, but it was not included as one of the features so the model was much less informed. Other algorithms should be considered for predicting cow IDs. 