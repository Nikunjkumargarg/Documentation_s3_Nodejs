# Create Bucket

<mark style="color:green;">`POST`</mark> /api/buckets

**Body**

This Api helps creating buckets. User can build both Private and Public Buckets.

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
