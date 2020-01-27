# LTFS-Data-Science-FinHack-2
![image](https://user-images.githubusercontent.com/37707687/73077779-da0e6c80-3ee6-11ea-9df0-a5b72de51cf8.png)
LTFS receives a lot of requests for its various finance offerings that include housing loan, two-wheeler loan, real estate financing and micro loans. The number of applications received is something that varies a lot with season. Going through these applications is a manual process and is tedious. Accurately forecasting the number of cases received can help with resource and manpower management resulting into quick response on applications and more efficient processing.

You have been appointed with the task of forecasting daily cases for next 3 months for 2 different business segments aggregated at the country level keeping in consideration the following major Indian festivals (inclusive but not exhaustive list): Diwali, Dussehra, Ganesh Chaturthi, Navratri, Holi etc. (You are free to use any publicly available open source external datasets). Some other examples could be:
Weather, Macroeconomic variables. Note that the external dataset must belong to a reliable source.

## Data Dictionary
The train data has been provided in the following way:
  - For business segment 1, historical data has been made available at branch ID level
  - For business segment 2, historical data has been made available at State level.
 
## Train File

| Variable             |  Definition        |
| ---------------------| -------------------|
| application_date     | Date of application     |
| segment              | Business Segment (1/2)     |
| branch_id            | Anonymised id for branch at which application was received     |
| state                | State in which application was received (Karnataka, MP etc.)     |
| zone                 | Zone of state in which application was received (Central, East etc.)     |
| case_count           | (Target) Number of cases/applications received  |

## Test File
Forecasting needs to be done at country level for the dates provided in test set for each segment.

| Variable             |  Definition        |
| ---------------------| -------------------|
| id                   | Unique id for each sample in test set     |
| application_date     | Date of application     |
| segment              | Business Segment (1/2)     |

## Sample Submission
This file contains the exact submission format for the forecasts. Please submit csv file only.

| Variable             |  Definition        |
| ---------------------| -------------------|
| id                   | Unique id for each sample in test set     |
| application_date     | Date of application     |
| segment              | Business Segment (1/2)     |
| case_count           | (Target) Predicted values for test set  |

## Evaluation
The evaluation metric for scoring the forecasts is MAPE (Mean Absolute Percentage Error) M with the formula:
![image](https://user-images.githubusercontent.com/37707687/73078359-0aa2d600-3ee8-11ea-8a94-aa5fb0c9f5dd.png)
Where At is the actual value and Ft is the forecast value.
The Final score is calculated using MAPE for both the segments using the formula:
![image](https://user-images.githubusercontent.com/37707687/73078449-31f9a300-3ee8-11ea-90d6-7fdf75c7c0b4.png)

### Important Notes
Note that feasibility of implementation of top solutions will be considered while adjudging winners. The solution must produce satisfactory results for both the business segments.

## Public and Private Split
Test data is further divided into Public (1st Month) and Private (Next 2 months)
Your initial responses will be checked and scored on the Public data.
The final rankings would be based on your private score which will be published once the competition is over.

## Leaderboard
- Public Leaderboard: 22/883 
- Private Leaderboard: 25/883

