# Get all buckets

<mark style="color:green;">`GET`</mark> /buckets

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/buckets' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjY1ZWZkNzIxLWEyYTQtNGRhMS05ZTYxLThkYTIyN2Q5ZTMyNyIsImlhdCI6MTcyMTUzNzI5MSwiZXhwIjoxNzIxNTM4MTkxfQ.bHVJGxVC0EMAdd5xDYHFeKMD9OrtM3v4avCzYWdNk9U'
```
{% endtab %}
{% endtabs %}

**Body**

This Api provides all users buckets. Only userId in the param is required.

**Response**

{% tabs %}
{% tab title="200" %}
```json
[
    {
        "id": "82169328-d6b4-40da-8747-87f01e37c9c9",
        "createdAt": "14:43:09",
        "name": "arjun",
        "userid": "d971f1a3-0128-409f-b83f-13b0dbbf9b34",
        "is_private": true,
        "updatedAt": "2024-07-21T16:16:02.000Z"
    }
]
```
{% endtab %}
{% endtabs %}
