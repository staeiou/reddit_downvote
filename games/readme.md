SELECT author, author_flair_text, ups, downs, created_utc, score, link_id, gilded, controversiality FROM [fh-bigquery:reddit_comments.2013] 
where subreddit = 'Games' 
AND created_utc BETWEEN TIMESTAMP_TO_SEC(TIMESTAMP("2013-01-01 00:00:00")) AND TIMESTAMP_TO_SEC(TIMESTAMP("2013-02-01 00:00:00")) 

SELECT author, num_comments, score, ups, downs, gilded, created_utc FROM [fh-bigquery:reddit_posts.full_corpus_201509] 
where subreddit = 'Games' 
AND created BETWEEN 1356998400 AND 1359676800
