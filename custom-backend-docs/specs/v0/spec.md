# v0 Specification

This `v0` specification is only for prototyping & is not intended to be treated as production ready in any manner...

all the route in v0 spec should be prefix with `{BASE_URL}/v0/`.


# Routes

## Passwords

### POST /passwords

It is use by passcodes app to post the data of single password entity that needs to be saved by server.

**Responsible**:

for saving the password entity on backend, this should return the saved password entity's id. 

**Request**:

will be a post request with just a body.

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
    
    ```json
    {
        "id": "int"
        "domain": "string",
	    "username": "string",
	    "password": "string",
	    "notes": "string",
        "created-at": "string",
        "updated-at": "string",
    },
    ```

**Note**:

We don't care for duplicates atleast for now. We in next specification version will provide a way, 
To let you send a specific status code when there is duplicates. It would be probably 400 BAD REQUEST.

---

### GET /passwords

It is use by passcodes app to get all the passwords previously saved by user.

**Responsible**:

for retriving all the passwords previously saved by user from backend. 

**Request**: 

will be a GET request with no query, path or any other parameters.

**Responses**:

- 200 OK
    
    In ideal cases the api should, return all the passwords.
    
    ```json
    [
        {
            "id": "int",
            "domain": "string",
            "username": "string",
            "passwords": "string",
            "notes": "string",
            "created-at": "string",
            "updated-at": "string",
        },
        ....
    ]
    ```

**Note**:

The authentication, pagination or query parameters based filter is not required currently. 
As this api specification is just for prototyping, but we will later add this features... 
If you can add there support from now itself then its good. 
but be sure that our app may still expect this api specification, without any extra fancy feaures.

---

### GET /passwords/:id

It is used by passcodes app to retrive single passwords entity.

**Responsible**: 

for getting the a password entity by its id.

**Request**:

will be a get request with a `:id` as a path parameter.

**Responses**:

- 200 OK

    In ideal cases the api should, return the password entity in response body.

    ```json
    {
        "id": "int",
        "domain": "string",
        "username": "string",
        "passwords": "string",
        "notes": "string",
        "created-at": "string",
        "updated-at": "string",
    },
    ```


- 404 NOT FOUND

    In cases where resource(password) not exist, the api should return 404.

**Note**:

...

---

### PUT /passwords/:id

It is used by passcodes app to update the data of a specific password entity.

**Responsible**:

for updating the password entity by its id.

**Request**:

will be a put request with a `:id` as a path parameter.

**Responses**:

- 200 OK
	
    In ideal cases the api should, return the updated password entity in response body.

    ```json
    {
        "id": "int",
        "domain": "string",
        "username": "string",
        "passwords": "string",
        "notes": "string",
        "created-at": "string",
        "updated-at": "string",
    }, 
    ```

- 404 NOT FOUND
	
    In cases where resource(password) not exist, the api should return 404.


**Note**:

...

---

### DELETE /passwords/:id

It is used by passcodes app to delete data of a specific password entity.

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

