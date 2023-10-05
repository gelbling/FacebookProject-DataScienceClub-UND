# Facebook Project - Data Science Club of Notre Dame
Developed software that predicts company’s LinkedIn post’s engagement through follower count, reactions,  comments, and hashtag data using machine learning and Python.

## Data

### Company Data
Contains information about the company:
  Number of followers
  Number of connections
Contains information about LinkedIn Company pages posts:
  Content of the post
  Number of hashtags used
  Number of reactions
  Number of comments

### Influencers Data
Contains information about the influencer:
  Number of followers
  Number of connections
Contains information about LinkedIn Influencers’ posts:
  Content of the post
  Number of hashtags used
  Number of reactions
  Number of comments

### Popularity Metric
- A  metric that is a weighted average of reactions and comments was created for both datasets
- This metric is used as a proxy for the popularity of each post

---

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/86b9c089-99f7-4420-8505-90de3c0ff0dc)

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/86f42f1e-359e-43f2-9448-9a05b8db33b0)

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/caa240dc-f097-43cb-b39f-068fa5ba460c)

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/b4905cfa-3417-434e-a020-1616a8564f16)

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/ca92ef1a-1f01-4d8c-bdee-f4ff7398a898)

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/ef37ee8c-9fa2-4408-9a89-ba9f34dc28df)

![image](https://github.com/gelbling/FacebookProject-DataScienceClub-UND/assets/23767501/ec6fb6ef-e280-4422-aee2-b2949488559b)

---

### Key Takeaways
- Low relative frequency, brand-specific hashtags show that there are not specific hashtags among popular posts that attract activity
- Specific brand and content are like drivers of high activity, not use of certain hashtags

## Modeling

### Goals
  Goal is to accurately measure popularity through LinkedIn
  Continuous, quantitative y-variable using various predictors in data set
  Measure popularity based on comments and reactions
  Assigned weights 
      Weight of comments: ⅔
      Weight of reactions: ⅓
  Assigned greater weight to the comments due to extra effort it takes to write a comment
  Popularity does not distinguish between positive and negative interactions 
  Only using the company data

### Preprocessing
  Filtered out all rows with time less than one day
      Note: May create minimal bias
  Change all quantitative data from strings to floats
  Remove commas in large numbers
  Drop unnecessary columns
      Location, media_type, about, media_urls, hashtags, etc.
  Split data into training and testing sets

### Preliminary Model
    Original Model: Decision tree regressor 
    Predictors: followers, connections, number of hashtags
    R^2: 0.2257747647065554
    MSE: 203874.616921866

### Preliminary Model
    Second Model: Random Forest 
    Predictors: followers, connections, number of hashtags
    MSE: 205996.68259815138

### Preliminary Model
    Second Model: Linear Model
    Predictors: followers, connections, number of hashtags
    R2: 0.012472456696375881
    MSE: 103468.70309077845

### Key Takeaways 
- Followers, connections, number of hashtags did not seem to be strong predictors of popularity by themselves
- The content of the post may be more useful in predicting popularity 

---

## Further Steps
    Including the content of the post in the model
    We are working on pre-processing the content
        Lowercasing
        Removing punctuation
        Removing stopwords 
        Tokenizing 
    Considering hashtags

---

## Benefits
    Why is understanding how to predict the popularity of a post important?
    Social media would be able to better make recommendations to companies looking to grow their platform about what type of posts users tend to interact with
        Improve the user experience for companies
        Help companies produce content to reach other uses and that other users are interested in 












