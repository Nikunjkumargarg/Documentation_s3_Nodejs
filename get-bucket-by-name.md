# Get bucket by name

<mark style="color:green;">`GET`</mark> /buckets/\<bucketname>

**Body**

This Api provides all users buckets. Only userId in the param is required.

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "id": "d1535c5c-e841-47d3-8be0-b2f039452432",
    "createdAt": "05:51:00",
    "name": "arjun",
    "userid": "1c8c07b8-88e3-4844-911e-8f1aef89b886",
    "is_private": true,
    "updatedAt": "2024-07-22T05:50:59.000Z"
}
```
{% endtab %}
{% endtabs %}
