# Development of a security system using number-plate recognition
Our idea is the development of a system of a transport-pass control, which will automatically register an arriving car without human intervention. Our project includes the model of the independent architectural system of separate components using number-plate recognition framework, to create a turnkey solution for private sectors. 
This system can be used by companies and individuals, who can put it in their located area. It generates an additional security system in their private yards, to control arrived transport. Our model consists of 3 main components:
1. NPR Server for number-plate recognition of received image;
2. CRM Web App - as a bridge to interact with a user, and communicate between I/O Service app with the server;
3. I/O Service app - to control periphery devices, such as camera and proximity sensor. 
NPR Server is built up using the Flask server and number-plate recognition framework, based on RNN, which will respond to the accepted request, containing the image of a number-plate, with the processed information, containing the number-plate in a text format. Users will not use it directly.
CRM Web app will be as a control panel to the user, which will show him the history of visits, add the list of allowed cars, etc. It is also used to redirect the request, came from I/O service app to the NPR Server. It was written using the Laravel framework. 
I/O Service app is used to monitor the arrived car and capture the image of it when it is needed. Service is written on C# language using .NET Framework.
