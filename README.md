# fake-apis-json-server
How to create a Fake REST API with JSON-Server


When you hit http://localhost:3000, 

Let’s go ahead and create a simple REST API that performs all CRUD operations-GET/POST/PUT/DELETE

GET
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