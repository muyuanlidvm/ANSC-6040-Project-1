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
          - Training set: 70% of rows with cow ID (randomly selected)
          - Validation set: 30% of rows with cow ID (randomly selected)
   
    - Model training:
      
          - Supervised learning to predict cow IDs

    - Model testing
 
    - Model performance
      
          - Accuracy
 
    - **Outcome**: generating a model that would predict cow ID based on all variables presented and complete the cow ID column of the dataset.
    
    *Week 6 (9/28)*: apply machine learning for problem solving. Specifically for days in milk (DIM), reproductive status (RPRO), and lactation number (LACT).
  
    *For each outcome variable:*
  
    - Splitting dataset:
 
          - Test set: rows without DIM/RPRO/LACT
          - Training set: 70% of rows wihtout missing data (randomly selected)
          - Validation set: 30% of rows wihtout missing data (randomly selected)
   
    - Model training:
      
          - Unsupervised learning to cluster cows
      
    - Model testing
 
    - Model performance (e.g., accuracy)
 
    - **Outcome**: If rows from cows with the same ID are clustered, will the model be able to fill-in-the-gap for DIM/RPRO/LACT? 
    
    *Week 7 (10/5)*: project summary, troubleshooting, preparation for poster presenetation.
  
- Methods:
    VS code will be used. Changes will be made locally then pushed to the cloud. 
