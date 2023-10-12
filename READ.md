Sinclair Schanne Corpuz

# GitHub REST API
The GitHub REST API is a web-based service that allows developers to interact with and manage GitHub repositories, issues, users, and various other resources.

## API Description

The GitHub REST API provides a wide range of functionalities for interacting with GitHub repositories and user accounts. Developers can use this API to create, read, update, and delete repositories, manage issues and pull requests, search for users and repositories, and much more. It's a versatile tool for integrating GitHub features into custom applications and 

## Api Endpoints

The GitHub API offers various endpoints for different tasks, including:

GET /repos/{owner}/{repo}: Retrieve information about a specific repository.
GET /users/{username}: Retrieve information about a GitHub user.
GET /issues/{owner}/{repo}: Retrieve a list of issues for a specific repository.
POST /repos/{owner}/{repo}/issues: Create a new issue in a repository.
And many more endpoints for different GitHub features.

## Request Payload

{
  "title": "New Issue",
  "body": "This is a description of the issue."
}
.

## API Response

{
  "name": "repository-name",
  "description": "A brief description of the repository",
  "owner": {
    "login": "username"
  }
}





## USAGE

import requests

url = 'https://api.github.com/repos/{owner}/{repo}'
response = requests.get(url)
data = response.json()
print(data)


## JSON Payload printName:
 
- Request payload:

This payload does not contain any specific fields. It might be used for retrieving or printing a name from the system, but the payload itself does not specify any required or optional fields.

## JSON Payload updateName:

- Request payload:
{
  "id":1,
  "lname":"corpuz",
   "fname":"sinclair"
}

This payload is used for updating an existing name entry identified by the specified "id". It requires the updated last name ("lname") and first name ("fname") of the person.

## JSON Payload deleteName:

- Request payload:
{
  "id":1
}

This payload is used for deleting a name entry based on the specified "id". It only requires the unique identifier of the name entry to be deleted.

## Response

## JSON Payload postName:

- Response payload:
{
         "status":"success","data":null
}

"status": Indicates the status of the API request. In this case, it's "success" indicating that the request was successful.
"data": This field is present but set to null, indicating that no specific data is returned for successful postName requests.

## JSON Payload printName:

- Response payload:
{
         "status":"success","data":["lname":"hortizuela","fname":"manny","lname":"corpuz","fname":"sinclair"]
}

"status": Indicates the status of the API request. It's "success" indicating that the request was successful.
"data": An array containing objects, each representing a name entry. Each object contains "lname" (last name) and "fname" (first name) fields with corresponding values. The response includes multiple name entries.


## JSON Payload updateName:

- Response payload:
{
         "status":"success","data":null
}

"status": Indicates the status of the API request. It's "success" indicating that the request was successful.
"data": This field is present but set to null, indicating that no specific data is returned for successful updateName requests.


## JSON Payload deleteName:

- Response payload:
{
         "status":"success","data":null
}

"status": Indicates the status of the API request. It's "success" indicating that the request was successful.
"data": This field is present but set to null, indicating that no specific data is returned for successful deleteName requests.



## Usage

import requests

url = 'https://api.github.com/repos/{owner}/{repo}'
response = requests.get(url)
data = response.json()
print(data)

## License

The GitHub REST API is typically used in accordance with GitHub's Terms of Service.

## Contributers

-Sir Manny Hortizuela(Provider)
-Jonafel Opinaldo(Collaborator)

## Contact Information

Include contact information for inquiries or support.

-Sinclair Schanne Corpuz

-sinclairschanne.corpuz@student.dmmmsu.edu.ph
-09952673342



