# User Login

## User is required to login with registered credentials to get access token and refresh token.

All API'S ARE AUTHORISED USING JWT ACCESS TOKEN.

<mark style="color:green;">`POST`</mark> /api/register

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/login' \
--header 'Content-Type: application/json' \
--data '{
    "username":"nikunj",
    "password":"gauriii"
}'
```
{% endtab %}
{% endtabs %}

**Body**

| Name     | Type   | Description          | Required |
| -------- | ------ | -------------------- | -------- |
| username | string | username of the user | Yes      |
| password | string | password of the user | Yes      |

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCyJ1c2VybmFtZSI6ImdhdXJpIiwidXNlcmlkIjoiZDk3MWYxYTMtMDEyOC00MDlmLWI4M2YtMTNiMGRiYmY5YjM0IiwiaWF0IjoxNzIxNTc2NTUzLCJleHAiOjE3MjIxODEzNTN9.a73upKf7Z5ysbJ5oFo4ZiWwQqGXFJqM6hduzi84C1N0",
    "refreshToken": "eyJhbGciOiJIUzI1NiIsI.eyJ1c2VybmFtZSI6ImdhdXJpIiwidXNlcmlkIjoiZDk3MWYxYTMtMDEyOC00MDlmLWI4M2YtMTNiMGRiYmY5YjM0IiwiaWF0IjoxNzIxNTc2NTUzLCJleHAiOjE3MjIxODEzNTN9.f2iVMOqpoSke7gezfP9KV33hY9aWvAnXkJLfq8oc4Q8"
}
```
{% endtab %}

{% tab title="400" %}
```json
{
    "errors": [
        {
            "type": "field",
            "value": "",
            "msg": "Username is required.",
            "path": "username",
            "location": "body"
        }
    ]
}
```
{% endtab %}
{% endtabs %}
