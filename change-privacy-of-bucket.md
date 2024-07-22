# Change privacy of bucket

## This api helps changing the privacy of user bucket. For eg. public to private and private to public bucket.

<mark style="color:green;">`PUT`</mark> /api/changePrivacy

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location --request PUT 'http://localhost:3000/api/changePrivacy' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImdhdXJpIiwidXNlcmlkIjoiZDk3MWYxYTMtMDEyOC00MDlmLWI4M2YtMTNiMGRiYmY5YjM0IiwiaWF0IjoxNzIxNTc2NTUzLCJleHAiOjE3MjIxODEzNTN9.a73upKf7Z5ysbJ5oFo4ZiWwQqGXFJqM6hduzi84C1N0' \
--data '{
    "bucketName":"arjun",
    "newPrivacy":true
}'
```
{% endtab %}
{% endtabs %}

**Body**

| Name       | Type    | Description                           | Required |
| ---------- | ------- | ------------------------------------- | -------- |
| bucketName | string  | name of the bucket                    | Yes      |
| newPrivacy | boolean | <p>true: private<br>false: public</p> | Yes      |

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "success": true,
    "message": "Bucket 'arjun' privacy updated successfully."
}
```
{% endtab %}
{% endtabs %}
