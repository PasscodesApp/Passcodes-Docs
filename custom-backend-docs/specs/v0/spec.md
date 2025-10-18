# v0 Specification

This `v0` specification is only for prototyping & is not intended to be treated as production ready...

all the route in v0 spec should be prefix with
`{BASE_URL}/v0/`

# Routes

## Passwords
### Get /passwords

It is use by passcodes app to get all the passwords previously saved by user.

**Responsible**: 
for return all the passwords previously saved by user. 

**Request**: 
will be a typical get request with no query or path or any other parameters.

**Responses**:
- 200 OK
	In ideal cases the api should, return all the passwords.

**Note**:
The authentication, pagination or query parameters based filter is not required currently, As it is just a prototyping api spec but we will add them later... if you can add there support from now itself. but should not be required.
### Post /passwords

It is use by passcodes app to post the data of single password entity that needs to be saved by server.

**Responsible**: 
for saving the password entity and also should return the password entity with id saved. 

**Request**:
will be a typical a post request with just a body.
```json
{
    "domain": "string",
	"username": "string",
	"password": "string",
	"notes": "string"
}
```

**Responses**:
- 201 CREATED
	In ideal cases the api should, return the id in response body.

**Note**:
We don't care for duplicates currently, we in next specification version will provide a way, to let you send a specific status code when there is duplicates. it would be probably 400 BAD REQUEST.

### Get /passwords/:id

It is used by passcodes app to get data of a specific single passwords data entity.

**Responsible**: 
for getting the single password entity by its id.

**Request**:
will be typically a get request with a `:id` as a path parameter.

**Responses**:
- 200 OK
	In ideal cases the api should, return the password entity in response body.
- 404 NOT FOUND
	In cases where resource(password) not exist, the api should return 404.

**Note**:
We don't care for duplicates currently, we in next specification version will provide a way, to let you send a specific status code when there is duplicates. it would be probably 400 BAD REQUEST.

### Put /passwords/:id

It is used by passcodes app to update the data of a specific single passwords data entity.

**Responsible**: 
for updating the single password entity by its id.

**Request**:
will be a put request with a `:id` as a path parameter.

**Responses**:
- 200 OK
	In ideal cases the api should, return the updated password entity in response body.
- 404 NOT FOUND
	In cases where resource(password) not exist, the api should return 404.

**Note**:
....

### Delete /passwords/:id

It is used by passcodes app to delete data of a specific single passwords data entity.

**Responsible**: 
for deleting the single password entity by its id.

**Request**:
will be a delete request with a `:id` as a path parameter.

**Responses**:
- 204 NO CONTENT
	In ideal cases the api should, return no body.
- 404 NOT FOUND
	In cases where resource(password) not exist, the api should return 404.

**Note**:
....

