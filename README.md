Connected Cars Platform Developer: Online Assignment

The requirement of our application is to create a Microservices backend to securely store data in a file format and allow the user to read and update when required. The backend should support storing the data in both CSV and XML file format.
Our application should contain 2 Microservices projects which have to be independently built & deployable and should follow the below functionality.

Service 1:
1.	This will be consumer-facing service which will accept request from the user.
2.	The service should accept the data in JSON format within the request body.
3.	The service should also accept another input fileType as a parameter or header within the request. The value to this parameter could be either CSV or XML.
4.	The service should expose 3 endpoints as below
a.	Store – to save new data
b.	Update – to update existing data
c.	Read – to read existing data, Read need not contain the fileType header or parameter
Note the request itself could contain any data. Sample given below can be used.
Sample body:
{ name: “Hello”, dob: “20-08-2020”, salary: “122111241.150”, age: 20 }
Request Header or Parameter
fileType = CSV
fileType = XML
5.	The service should process the request received with the below constraints.
a.	Validate the request completely. Including the data and data types
b.	Pass on the validated information to Service 2. Below are the conditions to keep in mind.
i.	The communication between Service 1 & Service 2 should NOT be http or https. Use some other means of communication.
ii.	The data transferred to the second service should be encrypted and transformed to Google’s protocol buffer format.
iii.	Only READ operation can be done over http
Service 2:
1.	Service should receive and decrypt the information passed by the previous service.
2.	Once decrypted the service should store the information either in CSV/XML file based on the input received in the fileType parameter in the previous service.
3.	If the data should be read and returned then the returned data has to be encrypted. Which Service 1 should decrypt and respond to the consumer.

Additional Tasks
1.	Please provide sufficient Junit to test everything
2.	README Documentation explain how to setup and execute the service.
3.	Please upload the code on the GIT HUB Platform and request you to keep the link Public for our Technical Team to review.



