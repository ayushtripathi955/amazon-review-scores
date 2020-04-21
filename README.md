# amazon-review-scores

Herein I created a MongoDB database called "amazon" that reads a select number of amazon reviews, each of them as a separate document, to the collection "reviews"  in the database "amazon".  Then I used MongoDB's map reduce function to build a new collection "avg_scores" that averages review scores by product ("asin") and subsequently a new collection called "weighted_avg_scores" that averages review scores by product ("asin"), weighted by the number of helpful votes. To average review scores based on weightage I used the base weight as 1 and for every additional helpful vote added 1 to the weight. 

The source of select Amazon Reviews that were used to compute review scores is of the following format:

• reviewerID - ID of the reviewer, e.g. A2SUAM1J3GNN3B
• asin - ID of the product, e.g. 0000013714
• reviewerName - name of the reviewer
• helpful - helpfulness rating of the review, e.g. 2/3
• reviewText - text of the review
• overall - rating of the product
• summary - summary of the review
• unixReviewTime - time of the review 
