# Refresh token

## This api is used to refresh the expired token of the user.

<mark style="color:green;">`POST`</mark> /api/refreshtoken

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/refreshtoken' \
--header 'Content-Type: application/json' \
--data '{
    "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjFjOGMwN2I4LTg4ZTMtNDg0NC05MTFlLThmMWFlZjg5Yjg4NiIsImlhdCI6MTcyMTYyNzQwOCwiZXhwIjoxNzIyMjMyMjA4fQ.nhDqJkhX0Tx2guTARQTlhk-B-LYSNtmkifT8rrtM8aU"
}'
```
{% endtab %}
{% endtabs %}

**Body**

| Name         | Type   | Description                                 | Required |
| ------------ | ------ | ------------------------------------------- | -------- |
| refreshToken | string | refresh token string received while log in. | Yes      |

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjFjOGMwN2I4LTg4ZTMtNDg0NC05MTFlLThmMWFlZjg5Yjg4NiIsImlhdCI6MTcyMTYzMjYxNiwiZXhwIjoxNzIxNjMzNTE2fQ.Q0CEnPl32NrSnTRQBPbTt2HiiEdZ8wHjBO4KCIVQIaI"
}    
```
{% endtab %}
{% endtabs %}
