# fake-apis-json-server
How to create a Fake REST API with JSON-Server


When you hit http://localhost:3000, 

Let’s go ahead and create a simple REST API that performs all CRUD operations-GET/POST/PUT/DELETE

# GET

Open the db.json file and replace the content with the following:

{
	“users”: [
				{
				“id”: 1,
				“firstName”: “Sachin”,
				“lastName”: “Tendulkar”,
				“age”: 45
				},
				{
				“id”: 2,
				“firstName”: “Alastair”,
				“lastName”: “Cook”,
				“age”: 37
				},
				{
				“id”: 3,
				“firstName”: “Steve”,
				“lastName”: “Smith”,
				“age”: 32
				}
			]
}

Refresh the browser window where your local server is running. You should see only one resource: users with a count of 3.

Open Postman and make a GET request- http://localhost:3000/users. You should 3 users as a result.Image for post

You can also perform operations such as sorting, filtering, searching, etc. Below are some of the examples:

* http://localhost:3000/users/2 (Returns the user with id-2)
* http://localhost:3000/users?_limit=2 (Sets the limit to return 2 records)
* http://localhost:3000/users?_sort=firstName&_order=desc (Sorts the records with the first name in descending order)
* http://localhost:3000/users?age_gte=40 (Returns the users whose age ≥40). Similarly you can set for age_lte and age_gte&age_lte
* http://localhost:3000/users?q=Sachin (Returns the users which contain the string “Sachin”)





# POST

Let’s add one new user to the users request.
Open a new tab in Postman and run the query (http://localhost:3000/users) with the POST operation. 
You need to set the header: Content-Type as application/json. 
In the body, select the body type as raw and add the following content:

	{
		“id”:4,
		“firstName”:”Rohit”,
		“lastName”:”Sharma”,
		“age”:32
	}

If you make a GET call, you should see 4 users now.

# PUT

Let’s modify the record with id 1
Open a new tab in Postman and run the query (http://localhost:3000/users/1) with the PUT operation. 
You need to set the header: Content-Type as application/json. 
In the body, select the body type as raw and add the following content:

	{
		“firstName”:”Sachin”,
		“middleName”:”Ramesh”,
		“lastName”:”Tendulkar”,
		“age”:47
	}
	


# DELETE

Let’s try to remove the user with id 3
Open a new tab in Postman and run the query (http://localhost:3000/users/3) with the DELETE operation.
The response is returned as empty {} object. 
This indicates that the object with the respective id is successfully deleted

If you make a GET call, you should only see 3 users now.

# PATCH
Let’s modify the first name of the record with id 2
Open a new tab in Postman and run the query (http://localhost:3000/users/2) with the PATCH operation. 
You need to set the header: Content-Type as application/json. 
In the body, select the body type as raw and add the following content:
	{
		“firstName”: “Test”
	}
	
If you make a GET call, you should only see the user with id 2 should have the first name as “Test”