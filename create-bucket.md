---
description: >-
  This Api helps creating buckets. User can build both Private and Public
  Buckets.
---

# Create Bucket

<mark style="color:green;">`POST`</mark> /api/bucket

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/bucket' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjFjOGMwN2I4LTg4ZTMtNDg0NC05MTFlLThmMWFlZjg5Yjg4NiIsImlhdCI6MTcyMTYyNzQwOCwiZXhwIjoxNzIyMjMyMjA4fQ.xKYkkC-4ooPz62in1Xx7v6lbxhNOl6j0jDhFt5KM7EY' \
--data '{
    "bucketName":"JKTECHNOLOGY",
    "isPrivate": true
}'
```
{% endtab %}
{% endtabs %}

**Body Payload**

| Name       | Type    | Description                                           | Required |
| ---------- | ------- | ----------------------------------------------------- | -------- |
| bucketName | string  | name of the bucket                                    | Yes      |
| isPrivate  | boolean | <p>true : private bucket,<br>false: public bucket</p> | Yes      |

**Bucket Naming Policy**

* Each user is allowed to create only one bucket with a specific name.
* Multiple buckets with the same name are not permitted for any user.

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "message": "Bucket created successfully"
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
            "msg": "Bucket name is required.",
            "path": "bucketName",
            "location": "body"
        },
        {
            "type": "field",
            "value": "",
            "msg": "Bucket name must be between 3 and 50 characters.",
            "path": "bucketName",
            "location": "body"
        }
    ]
}
```
{% endtab %}
{% endtabs %}
