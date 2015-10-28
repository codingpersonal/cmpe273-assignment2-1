# cmpe273-assignment2


#Setup

go get github.com/aggarwalsomya/cmpe273-assignment2/server

cd server

go run *


#Example to run


#CREATE

This will create a new location

curl -v -H "Content-Type: application/json"  -X POST -d '{"name":"saucy", "address":"1055 e evelyn ave", "city":"sunnyvale", "state":"ca", "zip":"94086"}' http://localhost:8081/locations


##OUTPUT

< HTTP/1.1 201 Created

< Date: Wed, 21 Oct 2015 07:32:01 GMT

< Content-Length: 171

< Content-Type: text/plain; charset=utf-8

{"_id":"3609","name":"saucy","address":"1055 e evelyn ave","city":"sunnyvale","state":"ca","zip":"94086","Coordinate":{"lat":"37.3679232","lng":"-122.0032597"},"error":""}





#GET:

This will get the details of location having an id 3609

curl -v -X GET http://localhost:8081/locations/3609

##Output

< HTTP/1.1 200 OK

< Date: Wed, 21 Oct 2015 07:33:41 GMT

< Content-Length: 171

< Content-Type: text/plain; charset=utf-8

{"_id":"3609","name":"saucy","address":"1055 e evelyn ave","city":"sunnyvale","state":"ca","zip":"94086","Coordinate":{"lat":"37.3679232","lng":"-122.0032597"},"error":""}




#PUT

This will update the location having an id 3609. 

curl -v -H "Content-Type: application/json"  -X PUT -d '{"address":"1 hacker way", "city":"menlo park", "state":"ca", "zip":"94025"}' http://localhost:8081/locations/3609


##Output

< HTTP/1.1 201 Created

< Date: Wed, 21 Oct 2015 07:35:07 GMT

< Content-Length: 175

< Content-Type: text/plain; charset=utf-8

{"_id":"3609","name":"saucy","address":"1 hacker way","city":"Menlo Park","state":"California","zip":"94025","Coordinate":{"lat":"37.4845750","lng":"-122.1479242"},"error":""}





#DELETE:


curl -v -X DELETE http://localhost:8081/locations/3609

This will delete the location having an id 3609. 

##Output: 

< HTTP/1.1 200 OK

< Date: Wed, 21 Oct 2015 07:37:55 GMT

< Content-Length: 0

< Content-Type: text/plain; charset=utf-8

 

