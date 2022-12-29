
##### Functional Requirements
* Hotel
  * Onboarding
  * Update properties ( add room, change pricing, add new Images etc)
  * Report to see bookings, revenue etc
* User
  * search for location based on filters like price range, star rating
  * Book hotel
  * Check booking
  * Analytics

##### Non Functional Requirement
* Low latency
* High Availability
* High Consistancy
* scale

#### System Design

* _UI -> LB -> Hotel Service -> (CDN for Image Storage, Mysql for Url Storage, Kafka)_
* _Search UI -> LB -> Search Service -> Elastic Search Server -> search consumer -> Kafka_
* _Book UI -> LD -> (Booking Service, payment Service) -> MySql -> Archival service -> kafka ->. Notification Service
* _Bookings UI -> LB -> Booking Management svc --> (redis, cassendra) -> kafka -> Hadoop

![Booking System Architecture Design](Airbnb+System+Design.png)

``` <img src="Airbnb+System+Design.png" alt="MarineGEO circle logo" style="height: 500px; width:900px;"/> ```
