
**Title**

### Signup a User

#### URL

```
api/v1/users/signup
```

#### Method

`POST`



#### URL Params


##### Required


##### Optional



#### Body
```json
{
	"username": "superman",
	"password": "password",
	"email": "test@mail.me",
	"active": "true",
	"role": "admin"
}
```


#### Success Response:



### Authenticate user
to authenticate a user, one should provide a username and provide and the response going to be a JWT Token to be used by the user to execute any request that require authentication

#### URL
```
/api/v1/users/authenticate
```
#### Method
` POST `

#### params 
 None
#### Body 
```json
{
  "username" : "superman",
  "password" : "p@ssw0rd"
}
```
#### Response
sucess: 200
content:
```json
{
  "JWT" : "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c"
}
``` 


### get User profiles

#### URL  
```
/api/v1/users/{uuid}/profiles
```
#### Method 
`GET`
####  params 
uuid -> User UUID **Required**
#### Body
 None
#### Response
content
```json
{
  "username": "username",
  "profiles": [
    {
      "uuid": "a2bf2e8c-4972-4bdc-b80b-5d81ba0bdfb3",
      "type": "student"
    },
    {
      "uuid": "f0bbc44a-54f5-4925-886a-d71889583262",
      "type": "assistant"
    }
  ]
}
```
