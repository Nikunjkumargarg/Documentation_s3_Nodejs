# Get bucket by name

<mark style="color:green;">`GET`</mark> /api/bucket/\<bucketname>

{% tabs %}
{% tab title="JavaScript" %}
```javascript
curl --location 'http://localhost:3000/api/bucket/JKTECHNOLOGY' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjFjOGMwN2I4LTg4ZTMtNDg0NC05MTFlLThmMWFlZjg5Yjg4NiIsImlhdCI6MTcyMTYyNzQwOCwiZXhwIjoxNzIyMjMyMjA4fQ.xKYkkC-4ooPz62in1Xx7v6lbxhNOl6j0jDhFt5KM7EY'
```
{% endtab %}
{% endtabs %}

**Body**

This Api provides all users buckets. Only userId in the param is required.

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "id": "d1535c5c-e841-47d3-8be0-b2f039452432",
    "createdAt": "05:51:00",
    "name": "JKTECHNOLOGY",
    "userid": "1c8c07b8-88e3-4844-911e-8f1aef89b886",
    "is_private": true,
    "updatedAt": "2024-07-22T05:50:59.000Z"
}
```
{% endtab %}
{% endtabs %}
