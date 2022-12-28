
#### Requirement Gathering

1. top sellers by entire site or by category? category or by sub-category
2. How uptodate expected to be? few times per day
3. trending and popular filter? yes
4. what is scale of transactions? thousands of hundered

#### System Design

##### Architecture Design

(aws s3 storage for item, category, date purchased) <- (top seller job using Spark) <- (top seller database) <- Distributed cache <- application
