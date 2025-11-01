# Sports Athlete Injury Analysis

DSA project template for the Bootcamp on Nov 1st, 2025. 

Provide a [[link to your dataset]("ziya07/athlete-injury-and-performance-dataset")](https://www.kaggle.com/datasets/ziya07/athlete-injury-and-performance-dataset) 

Briefly _explain_ your **hypothesis**.
# the more serve the injury, the lower the athlete's performance


## Sub headings

More info:
- item1
- item2

We will do the following:
1. number 1
2. number 2

# code 
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import numpy.random as rand

# import dataset
df = pd.read_csv("/collegiate_athlete_injury_dataset.csv")

# data cleanup
df.drop("Athlete_ID", axis=1, inplace=True)
df.drop("Injury_Indicator", axis=1, inplace=True)
df.drop("Load_Balance_Score", axis=1, inplace=True)
df.drop("ACL_Risk_Score", axis=1, inplace=True)
df = pd.DataFrame({"Position": ["Guard", "Center", "Forward"]})
df["Position"].value_counts().plot.pie()
