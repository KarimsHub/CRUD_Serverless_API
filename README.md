# AWS: CRUD (Create, read, update and delete) Serverless API with AWS Lambda, API Gateway and a DynamoDB

## Steps to follow:
1. Create a Dynamo DB Table with a partition key as string (for eg. productid)
2. Create a I am Role so the Lamda Function can access our Dynamo DB Table. Choose Lamda and attach two policies to it: Cloudwatchfullaccess and dynamodbfullaccess 
3. Create a lambda function and choose Python and the Role which we created before
4. After Creation you can change the mofification of the lamda function in case of memory and timeout to a minute for eg
5. Create a Rest API in API Gateway to connect everything
6. Choose new API and give it a name
7. Create new Paths (under create new Resource): for eg. /health, /product, /products and enable API Gateway CORS on all of them
8. Under the created Path, create a GET method whether to check for the user if the api is healthy or not. For that just create a new Method, use Lambda Function and click "Use Lambda Proxy Integration" and choose the Lambda Function which was created earlier (eg. severless-api-lambda)
9. After that we create a Post Method to insert into the database
10. Than we create a Patch Method to modify an item in th db
11. Last but not least a delete Method to delete items in the db
12. Now we have to deploy the API to make it active. For that you click on root --> actions --> deploy API
13. Createa a new stage and give it a name (eg. prod)





![ImgName](https://github.com/KarimsHub/Doubly_linked_list_datastructure/blob/master/sllvsdll.jpg?raw=true)

