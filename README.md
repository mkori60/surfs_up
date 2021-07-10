# Purpose
The purpose of this project is to produce analysis that supports a vision of opening a shop in Oahu, Hawaii that sells surf gear and ice cream. This project seeks to analyze weather data in order to determine if the surf shop is likely to succeed year round by analyzing precipitation and temperature rates. This project uses SQLite, SQLAlechemy, Python, Jupyter Notebook and Flask. 

## Results 
According to a key investor, W.Avy, high levels of precipitation resulted in his last surf shop being run out of business. Therefore, I began my analysis by producing summary statistics for the overall precipitation data. 

<img width="238" alt="Screen Shot 2021-07-10 at 1 55 46 PM" src="https://user-images.githubusercontent.com/83051034/125174998-8ea55800-e186-11eb-9ea0-e312db81e80e.png">

I also checked the temperature station used most frequently in order to ensure that my data was accurate. 
Next, I analyzed the temperature data for the months of June and December in order to identify any significant difference.

<img width="305" alt="Screen Shot 2021-07-10 at 1 58 10 PM" src="https://user-images.githubusercontent.com/83051034/125175151-57837680-e187-11eb-9489-9a1f517a09d3.png">

<img width="292" alt="Screen Shot 2021-07-10 at 2 00 44 PM" src="https://user-images.githubusercontent.com/83051034/125175142-42a6e300-e187-11eb-8cb7-19857b3aa6df.png">

Key differences:

* The mean temperature is approximately 3 degrees lower in December than June 
* The minimum temperature is 8 degrees lower in December than June
* The max temperature is 2 degrees lower in December than in June

I then created two further queries in order to produce precipitation data for the months of June and December in order to identify any major difference. 

<img width="263" alt="Screen Shot 2021-07-10 at 2 19 54 PM" src="https://user-images.githubusercontent.com/83051034/125175512-ed200580-e189-11eb-852d-70da8766dd5e.png">

<img width="188" alt="Screen Shot 2021-07-10 at 2 16 09 PM" src="https://user-images.githubusercontent.com/83051034/125175442-6539fb80-e189-11eb-991f-80f2441e6fa9.png">

I then got the number of days with rain for both June and December using the code: 

june_prcp_count = june_prcp_df[june_prcp_df['June Precipitation'] > 0].count()

There were 927 days out of 1574 that had rain in June, or 58.89 percent of the time. 

prcp_count = dec_prcp_df[dec_prcp_df['Dec Precipitation'] > 0].count()

There were 895 out of 1405 days with rain in December, or 63.7 percennt of the time. 

## Summary 
If W.Avy has not had a successful experience in the past due to rain, then the weather analysis suggests that the high number of rainy days in Oahu would make it difficult for the surf and icecream shop to succeed. However, the analysis does not show at what times during the day it rained. If it rained at night, then the shop still would be able to attract customers during the day. The weather year round is warm enough that the shop should be able to be successful as long as the rain does not interfere with customers. 
