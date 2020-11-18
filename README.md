# RESTProject1
[TC_001]To verify whether application allows the admin to get access token 
[TC_002]"TO verify whether application allows the admin to login into the system with valid credentials and get admin account details  
And log out of the system "

[TC_009] TO verify whether application allows the admin to add new customer then delete customer by id and then verify customer deleted
"In Customer service, call add new customer api endpoint
POST /customers"
Provide customer details request body
Use groovy script to fetch customer_id from add new customer api response and set custom property for customer_id
"In Customer service, call get customer details by id api endpoint
GET /customers/{id}"
Provide customer_id path parameter from custom property 
"In Customer service, call delete customer by id api endpoint
DELETE /customers/{id}"
Provide customer_id path parameter from custom property
"In Customer service, call get customer details by id api endpoint
GET /customers/{id}"
Provide customer_id path parameter from custom property
Add script Assertion to validate status code
Run the Test Case


[TC_010]TO verify whether application allows the admin to add new customer and then add rewards point to that customer
"In Customer service, call add new customer api endpoint
POST /customers"
Provide customer details request body
Use groovy script to fetch customer_id from add new customer api endpoint and set custom property for customer_id
"In Customer service, call get customer details by id api endpoint
GET /customers/{id}"
Provide customer_id path parameter from custom property 
"In Customer service, call add rewards points to customer api endpoint
POST /reward/{id}"
Provide customer_id path parameter from custom property
Provide reward details request body
"In Customer service, call get customer details by id api endpoint
GET /customers/{id}"
Provide customer_id path parameter from custom property
Add script Assertion to validate status code and customer_id, reward_points
Run the Test Case

