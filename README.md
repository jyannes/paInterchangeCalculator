Pennsylvania Toll Calculator 
This project is a cloud-based back-end implementation of a toll calculator. The toll calculator provides users with the cost of tolls for different payment options, distance, and driving time between two interchanges on a highway.

Architecture
The back-end of the toll calculator is built on a serverless architecture using AWS services. The architecture consists of the following components:

API Gateway: The API Gateway is the entry point for all incoming requests to the application. It receives HTTP requests from the front-end and triggers the appropriate Lambda function to handle the request.

Lambda Functions: Lambda functions are serverless compute units that run in response to events. In this application, there are three Lambda functions that handle different requests:

calculateToll: Calculates the toll for a given payment method and route.
getCoordinates: Retrieves the coordinates (latitude and longitude) of the entrance and exit interchanges.
getSunsetTime: Calculates the sunset time for a given location and date.
Amazon RDS: The Amazon RDS database stores the toll schedules for different payment methods. The database is used by the calculateToll Lambda function to retrieve toll rates.

Amazon S3: The Amazon S3 bucket stores the HTML and CSS files that are used to display the front-end of the application.

Amazon CloudWatch: CloudWatch is used to monitor and log Lambda function execution and API Gateway requests.

Deployment
The application is deployed using the AWS Serverless Application Model (SAM). The SAM template defines the infrastructure required for the application, including the API Gateway, Lambda functions, and database. The application is deployed to AWS using the sam deploy command.

Development
To run the application locally, you need to set up the following:

AWS CLI: The AWS CLI is used to interact with AWS services from the command line.
Docker: Docker is used to run the SAM CLI in a local environment.
SAM CLI: The SAM CLI is used to build and test the application locally.
To test the Lambda functions locally, you can use the sam local invoke command. To test the API Gateway locally, you can use the sam local start-api command.

Technologies
The back-end of the toll calculator is built using the following technologies:

AWS Lambda
API Gateway
Amazon RDS
Amazon S3
Amazon CloudWatch
AWS SAM
AWS CLI
Docker
Conclusion
The toll calculator back-end project is an example of a cloud-based serverless application that leverages the power of AWS services to provide a scalable and reliable back-end. This project demonstrates how to use AWS Lambda, API Gateway, and Amazon RDS to build a fully functional back-end for a web application.



