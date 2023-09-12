# USGS Testing Project
Testing different API requests from the page https://earthquake.usgs.gov.
There are different files for each type of request.

## Verify status
First test verifies if the status received it's OK.

Second test verifies if the number from the response is prime.

## Verify request
There are 3 tests. The request's url it's slightly written wrong. In the url "startime" should be written as "starttime".

First test verifies the request's status. The status gives a 400 Bad Request because the url request it's written wrong.

Second test verifies if the status it's OK. The test should fail.
It fails because it's gives 400 status and the test expects a 200.

Third test verify if the response body it's type JSON.
Gets the Content-Type from the Headers and checks if it is equal to to "application/json" to be equals.

## Exceeds the maximum number of earthquakes/tsunami
There are 2 similar test.

First test checks if the number of earthquakes exceeded the variable maxearthquakes.

Second test checks if the number of tsunamis exceeded the variable maxtsunamis.
Each earthquake has a variable tsunami that is false or true, and the test count all the tsunamis that are true.

## Shattering period in a zone
It verifies if the magnitute in a area it's over the variable maxmagnitude.

It takes the highest magnitude from the response and compares it to the variable maxmagnitude. 

## Earthquakes in Romania
Verifies if the number of earthquakes in Romania it's over 2, between the dates of 1977-03-04 and 1977-03-05.