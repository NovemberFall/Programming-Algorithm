## Exploring the dataset and identifying predictors

- Logically it relates to the audio version of books only each customer in the database
  has made a purchase

- Goal: create a machine learning model that predicts if a customer will buy again from
  the platform



![](img/2020-10-11-11-49-46.png)  

- for `audiobooks.csv`, each row represents a person
  - we have customer ID, here ID is like a name, we will skip it on my algorithm
  - we have book length OVERALL, booklengh for average, (sum divided by the number of purchase)
  - The # purchase = overall length / average length
  - The price variable is almost always a good predictor!
  - Review is a Boolean. It shows if the customer left a review (1 = left a review, 0 = didn't)
  - for Review 10/10, it measures the review of a customer from 1 to 10
    - we quickly see most people leave no review, as in most marketplaces
    - for our ML algorithm, 8.91 = status quo a review > 8.91 indicates above average "feelings"
    - a review < 8.91 indicates below average "feelings"
  - Last visited minus Purchase data: if it is 0, indicates the customer has never accessed whe 
    he/she has bought

- We are doing supervised learning so we need `targets`
  - Targets: `1` if a customer bought again in the last 6 months of data, `0` if a customer did 
    not buy again





