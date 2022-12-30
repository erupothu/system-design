
#### Functional Requirement
* tweets
* re-tweet
* follow
* search

#### Non Functional Requirement
* read heavy
* fast rendering
* fast tweets
* log ok in some cases
* scale
    * 150 miil DAU
    * 350 mill mav
    * 1.5 bill Accounts
    * 500 mill tweet/day
    
#### Users
* Famous
* Active
* Live
* Passive
* InActive

##### System Design

* Architecture Design

![Twitter Architecture Design](Twitter-System-Design.png)

* Frontend pages
    * User Onboarding/ Login Flow
    * User following flow
    * Adding Post UI
    * User Self profile screen
    * Home screen
    * search screen
    * User App screen

* Backend Services
    * User Service
    * Graph Service
    * Tweet Injection Service
    * short Url Service
    * Timeline Service
    * Asset service
    * Tweet service
    * Tweet processor
    * Analytics service
    * Live user websockets
    * trends
    * search kafka consumer
    * search service
    * Notification service

* Other serers
    * User DB
    * User Graph DB
    * redis
    * cassandra
    * kafka
    * Hadoop
    * Spark
    * Elastic search
