## User Service Documentation
**Title**
<Additional information about your API call. Try to use verbs that match both request type (fetching vs modifying) and plurality (one vs multiple).>

### Signup a User

#### URL

```
api/v1/users/signup
```

#### Method

`POST`



#### URL Params

<If URL params exist, specify them in accordance with name mentioned in URL section. Separate into optional and required. Document data constraints.>

##### Required:


##### Optional:

photo_id=[alphanumeric]

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

<What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!>

Code: 200 
Content: { id : 12 }
Error Response:

<Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be.>

Code: 401 UNAUTHORIZED 
Content: { error : "Log in" }
OR

Code: 422 UNPROCESSABLE ENTRY 
Content: { error : "Email Invalid" }
Sample Call:

<Just a sample call to your endpoint in a runnable format ($.ajax call or a curl request) - this makes life easier and more predictable.>

Notes:

<This is where all uncertainties, commentary, discussion etc. can go. I recommend timestamping 

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
  profiles: [
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
