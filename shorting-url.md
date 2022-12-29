

#### Gather Requiremnet..

1. Design a URL Shorting Service?
2. what is the traffic looking at?
3. How many unique urls come every day/month/year?
4. what duration you need save the url eg.10years?
5. you mean like bitly, everyone uses short url and will be redirecting them to actual url?
6. what is the scale of user everyday? millions
7. Any restriction on the characters on shorten url? (a-z 0-9 = 36 character 36^6 = 2176782336 url ~2billionn)
8. Own Urls allowed and can be created or deleted by themself.
9. User Login System?


#### Design  System

##### Performance Analytics
* save for 10 years
   * x_request x 60sec x 60min x 24hours x 365days x 10 years = y
   * __[a-z] + [A-Z] + [0-9] = 62 characters__
   * short url length = 6 then 62^6 = 3 trillion urls < y

##### API's required
1. Add new URL  - __POST__  
    * longUrl, userId -> status, shortURL  
2. Add new vanity URL - __POST__
    * longUrl, userId, vanityUrl -> status
3. Update URL - __PATCH__
    * longUrl, userId, updatedLongUrl -> status, shortUrl
4. Delete Url - __DELETE__
    * longUrl, userId -> status
5. Desplay Mapping - __GET__
    * longUrl, userId -> status, shortUrl
6. Redirect - __GET__
    * shortUrl -> redirect LongUrl

##### Database Schema design
1. m_url
      * id, userId, longUrl, shortUrl, status

##### Architecture Design
* __Frontend(web, mobile, tab) -> Discovery Service (load balancing) -> (service1a, service1b, ... service1N) -> Cache(Reddis)/token service -> NoSql Database(cassenra)__

#### Analytics and Reports
* Use Kafka good but more cpu and IO
* Dump all data into Hadoop and build Hive Queies aso spark stream jobs and do aggregation on it
* 





