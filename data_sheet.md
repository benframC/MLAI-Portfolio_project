# Datasheet

## Motivation

- For what purpose was the dataset created? 
ASHRAE compiled the dataset to be used for the Kaggle competition, AHSRAE - Great Energy Predictor III (https://www.kaggle.com/competitions/ashrae-energy-prediction/overview).
- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?
American Society of Heating, Refrigerating and Air-Conditioning Engineers (ASHRAE)

 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 
Metered energy usage; chilled water usage; steam usage; hot water usage; weather data; low context building metadata. 
- How many instances of each type are there? 
139772 rows of hourly meter readings and weather data over a single year. These correspond to 1448 unique buildings. 
- Is there any missing data?
There are sporadic NaNs amongst the weather data. Until May 20th 2016, meter '0' for buildings numbered below 105 are zero.
- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?
No.

## Collection process

- How was the data acquired? 
Unknown to data sheet author.
- If the data is a sample of a larger subset, what was the sampling strategy? 
Unknown to data sheet author.
- Over what time frame was the data collected?
All hours of the year 2016.

## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 
Unknown to data sheet author.
- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 
 
## Uses

- What other tasks could the dataset be used for? 
Finding correlations between energy usage and weather. 
- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 
No. 
- Are there tasks for which the dataset should not be used? If so, please provide a description. 
Unknown to data sheet author.

## Distribution

- How has the dataset already been distributed? 
Via Kaggle competition. 
- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  
License subject to Kaggle competition rules, found here: https://www.kaggle.com/competitions/ashrae-energy-prediction/rules. 

## Maintenance

- Who maintains the dataset?
ASHRAE. 

