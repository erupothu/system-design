
#### Requirement Gathering

1. one restarent or many restaurent? many  
2. scalable and reliable and falt load time system.  
3. analytics, reporting, how many table available.  


##### API Design
1. __POST__ create/update Register Customer
      * id, name, phone, email, location -> id, name, phone, email, location
2. __POST__ create/update Register Restaurent
      * id, name, address, phone, tables, timings
3. __GET__ List Default Restaurent nearest to user location
      * restaurentName, Address, phone, bussinessHours, availableTables, seats
5. __GET__ List restaurents by search by name  
      * restaurentId, restaurentName, Address, phone, bussinessHours, availableTables, seats
6. __POST__ book table
      * customerId, restaurentId, tableNo, seats

##### Database Design

1. m_restaurent
    * id, name, address, phone, tables, seats per table, bussiness_hours, reservation_length, walkup_holdback

2. m_customer
    * id, name, phone, email, prefences, location

##### Architecture Design

__frontend(mobile, web) -> api-gateway -> Discovery-service (load balancer) -> (service1a, service1b .... service1n) -> cache -> database__
