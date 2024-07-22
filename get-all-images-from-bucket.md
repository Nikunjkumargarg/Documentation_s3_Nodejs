# Get all Images from bucket

## This api helps inserting images in the bucket

<mark style="color:green;">`GET`</mark> api/buckets/\<bucketname>/objects

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/buckets/arjun/objects/' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjFjOGMwN2I4LTg4ZTMtNDg0NC05MTFlLThmMWFlZjg5Yjg4NiIsImlhdCI6MTcyMTYyNzQwOCwiZXhwIjoxNzIyMjMyMjA4fQ.xKYkkC-4ooPz62in1Xx7v6lbxhNOl6j0jDhFt5KM7EY'
```
{% endtab %}
{% endtabs %}

**Response**

{% tabs %}
{% tab title="200" %}
```json
[
    {
        "id": "1e34240a-4271-4931-945e-8e0c86e0841b",
        "createdAt": "06:10:33",
        "name": "COMMON RECRUITMENT PROCESS FOR RECRUITMENT OF CLERKS IN PARTICIPATING BANKS (CRP CLERKS-XIV).pdf",
        "url": "http://localhost:3000/api/buckets/arjun/objects/COMMON RECRUITMENT PROCESS FOR RECRUITMENT OF CLERKS IN PARTICIPATING BANKS (CRP CLERKS-XIV).pdf",
        "bucketName": "d1535c5c-e841-47d3-8be0-b2f039452432",
        "size": 377423,
        "updatedAt": "2024-07-22T06:10:33.000Z"
    },
    {
        "id": "9dde3106-1431-49e9-bee0-b7fe401bb718",
        "createdAt": "06:11:03",
        "name": "ABC.PDF",
        "url": "http://localhost:3000/api/buckets/arjun/objects/ABC.PDF",
        "bucketName": "d1535c5c-e841-47d3-8be0-b2f039452432",
        "size": 377423,
        "updatedAt": "2024-07-22T06:11:02.000Z"
    }
]
```
{% endtab %}

{% tab title="400" %}
```json
{
    "error": "Failed to retrieve file",
    "message": "Error getting file"
}
```
{% endtab %}
{% endtabs %}
