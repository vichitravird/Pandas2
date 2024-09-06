# Pandas2
## 1 Problem 1 : Article Views I	(	https://leetcode.com/problems/article-views-i/  )
<br>
import pandas as pd

def article_views(views: pd.DataFrame) -> pd.DataFrame:
    df=views[views['author_id']==views['viewer_id']]
    return df[['author_id']].rename(columns={'author_id':'id'}).drop_duplicates().sort_values(by='id')


## 2 Problem 2 :Invalid Tweets	(	https://leetcode.com/problems/invalid-tweets/ )
<br>
import pandas as pd

def invalid_tweets(tweets: pd.DataFrame) -> pd.DataFrame:
    df=tweets[tweets['content'].str.len()>15]
    return df[['tweet_id']]




