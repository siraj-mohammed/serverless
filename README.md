# Serverless Computing with AWS

## Description
This is a basic serverless app that utilizes various services available on AWS - namely Lambda, API Gateway, S3, and DynamoDB - for its functionality.
The app allows the user to add their favorite movie(s) to a list and then click the movie name to retrieve more information, such as Rating, Released Date and a Plot Summary, about that movie.

App URL: https://s3.amazonaws.com/moviesearch-msr/index.html

## The Architecture
*S3* - A static HTML, with embedded CSS and jQuery, is hosted on S3. This serves as the UI for the app. All front-end logic - user interaction, API call, formatting and displaying the server response - resides in this file.

*Lambda/API Gateway* - The 'server' logic is provided by a Lambda function which is responsible for listening to GET requests, extracting the movie title from the query, making an API call to OMDB, and passing the response back to the client. The lambda also adds a record to a table in DynamoDB for every query it processes. An API gateway is attached to the lambda that proxies all the queries and responses.

## App Demo
A short demo of the app:
![Serverless App](https://drive.google.com/file/d/10QwMgA-XxYylmmhJBTMWpwntl1ztv20K/preview)

## Tools/Technologies Used
- HTML/CSS/Bootstrap/jQuery
- Node.js/AWS-SDK
- AWS Lambda, S3, DynamoDB