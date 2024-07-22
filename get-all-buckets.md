# Get all buckets

<mark style="color:green;">`GET`</mark> /buckets

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
