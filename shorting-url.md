

#### Gather Requiremnet..

1. Design a URL Shorting Service?
2. you mean like bitly, everyone uses short url and will be redirecting them to actual url?
3. what is the scale of user everyday? millions
4. Any restriction on the characters on shorten url? (a-z 0-9 = 36 character 36^6 = 2176782336 url ~2billionn)
5. Own Urls allowed and can be created or deleted by themself.
6. User Login System?


#### Design  System

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
## Frontend(web, mobile, tab) -> Discovery Service (load balancing) -> (service1a, service1b, ... service1N) -> Cache(Reddis) -> NoSql Database





