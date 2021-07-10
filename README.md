# Mood-Based-Food-Recommender-System
Moody Foodies is a food recommendation system which recommends food based on the mood of the customer. It aims to overcome the customer’s paradox of choice by filtering down the options of food based on their current mood and demographics, additionally it also provides common food allergens info for the recommended dishes. The system generates recommendations using the data gathered through surveys and various other sources, as a next step the engine would find out the best restaurant options considering dish chosen, distance, affordability and rating as factors.

Primary Data Source: Survey - https://survey.zohopublic.in/zs/YDDw4Q

Secondary Data Sources – Swiggy, Recipes and common food allergens from google 


**Modelling:** 
•	K-Nearest Neighbor is one of the simplest Machine Learning algorithms based on Supervised Learning technique.
•	Depending on the Euclidean distance between the new data point and existing data points we find K nearest users who are similar, fetch the dishes chosen by these neighbors, create a frequency table and filter top N dishes as recommendations to the new user.


**Evaluation:**
Average Precision (AP@N):

•	If we are asked to recommend N items, the number of relevant items in the full space of items is m, then:
![image](https://user-images.githubusercontent.com/52981642/125155225-f6a27100-e17b-11eb-93cd-a7491c1e9a73.png)
 
•	where rel(k) is just an indicator that says whether that kth item was relevant (rel(k)=1) or not (rel(k)=0). I'd like to point out that instead of recommending N items we could have recommended, say, 2N, but the AP@N metric says we only care about the average precision up to the Nth item.

The MEAN in **MAP@N:**
•	Average Precision, applies to a single data point (like a single user), whereas MAP averages the AP@N metric over all the users. 
It’s an average of an average.

![image](https://user-images.githubusercontent.com/52981642/125155236-015d0600-e17c-11eb-97df-55faec0269cd.png)

Mean average precision (MAP@N) of our model is currently 10%, due to the limitation in survey data collection versus the number of classes we have in our data. As a future improvement we could improve the precision by collecting more survey data. 


Output of the recommender system on jupyter notebook:

![Moody Foodies Output](https://user-images.githubusercontent.com/52981642/125154999-a24ac180-e17a-11eb-88be-64fa5094254a.PNG)
