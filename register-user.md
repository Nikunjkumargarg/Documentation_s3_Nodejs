# Register User

## Create a new user

<mark style="color:green;">`POST`</mark> /api/register

**Body**

| Name     | Type   | Description          | Required |
| -------- | ------ | -------------------- | -------- |
| username | string | username of the user | Yes      |
| password | string | password of the user | Yes      |

**Response**

{% tabs %}
{% tab title="200" %}
```json
User registered
```
{% endtab %}

{% tab title="400" %}
```json
{
    "errors": [
        {
            "type": "field",
            "value": "",
            "msg": "Password is required.",
            "path": "password",
            "location": "body"
        },
        {
            "type": "field",
            "value": "",
            "msg": "Password must be at least 6 characters long.",
            "path": "password",
            "location": "body"
        }
    ]
}
```
{% endtab %}
{% endtabs %}