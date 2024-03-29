# Introduction
Chat application (Instant messaging system: this is school projects we developed in Year 3 to apply Human centered design skills in designing interactive and attractive user interfaces)
This phpChatApp Has an API which was built from the ground-up with a JSON API that makes it easy for developers and sysadmins To consume Provided Data .


## Use Cases

There are many reasons to use an API. 
Down Here , there are required Few things You Might Want to do with The API:

```http
GET :: USER BY USERNAME : chatapplicationgroup2/API.php?api_name=get_user&username=username
```

```http
GET :: ALL USERS chatapplicationgroup2/API.php?api_name=get_user&username=*
```

##### USING POST YOU CAN CHANGE USER THEME
```http
POST :: CHANGE USERS THEME chatapplicationgroup2/API.php?api_name=change_theme&username=blaise&theme=1
```





## Responses

#### SUCCESS RESPONSES
Many API endpoints return the JSON representation of the resources created or edited : 

```javascript
{
    unique_id	"2051224492162685558060f7d89cbcb6f"
    first_name	"Blaise"
    last_name	"NINDENKIMANA"
    username	"blaise"
    email	    "bnindenkimana2@gmail.com"
    avatar	    "9.svg"
}
```

#### FAILED RESPONSES
However, if an invalid request is submitted, or some other error occurs, A JSON response in the following format Will be returned

```javascript
{
    "status" => 'int',
    "success" => 'failed',
    "message" => "ERROR DESCRIBING THE REQUEST"
}
```


The `message` attribute contains a message commonly used to indicate errors or

The `success` attribute describes if the transaction was successful or not.

The `status` attribute describes if the transaction was successful or not.



## Status Codes

 Codes Describing the status errors which will be returned to you , 

| Status Code | Description |
| :--- | :--- |
| 200 | `OK` |
| 201 | `CREATED` |
| 400 | `BAD REQUEST` |
| 404 | `NOT FOUND` |
| 500 | `INTERNAL SERVER ERROR` |

