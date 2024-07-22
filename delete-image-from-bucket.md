# Delete Image from Bucket

## This api helps inserting images in the bucket

<mark style="color:green;">`DELETE`</mark> /api/buckets/\<bucketName>/objects/\<fileName>

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location --request DELETE 'http://localhost:3000/api/buckets/arjun/objects/COMMON RECRUITMENT PROCESS FOR RECRUITMENT OF CLERKS IN PARTICIPATING BANKS (CRP CLERKS-XIV).pdf' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImdhdXJpIiwidXNlcmlkIjoiZDk3MWYxYTMtMDEyOC00MDlmLWI4M2YtMTNiMGRiYmY5YjM0IiwiaWF0IjoxNzIxNTc2NTUzLCJleHAiOjE3MjIxODEzNTN9.a73upKf7Z5ysbJ5oFo4ZiWwQqGXFJqM6hduzi84C1N0'
```
{% endtab %}
{% endtabs %}

NOTE: If fileName is not provided in the param then image name will be considered as the uploaded image name, if passed in the params, then that will be the name of the image.

**Body**

| param      | Type   | Description                                      | Required |
| ---------- | ------ | ------------------------------------------------ | -------- |
| bucketName | string | name of the bucket from which the file to delete | Yes      |
| fileName   | string | name of the file to be deleted                   | yes      |

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "message": "File deleted successfully"
}
```
{% endtab %}

{% tab title="404" %}
```json
{
    "error": "File not found",
    "message": "File 'ABCD.PDF' not found in bucket 'arjun' for deletion."
}
```
{% endtab %}
{% endtabs %}
