# Get Image from bucket

## This api helps inserting images in the bucket

<mark style="color:green;">`GET`</mark> api/buckets/\<bucketname>/objects

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/buckets/arjun/objects/COMMON RECRUITMENT PROCESS FOR RECRUITMENT OF CLERKS IN PARTICIPATING BANKS (CRP CLERKS-XIV).pdf' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImdhdXJpIiwidXNlcmlkIjoiZDk3MWYxYTMtMDEyOC00MDlmLWI4M2YtMTNiMGRiYmY5YjM0IiwiaWF0IjoxNzIxNTc2NTUzLCJleHAiOjE3MjIxODEzNTN9.a73upKf7Z5ysbJ5oFo4ZiWwQqGXFJqM6hduzi84C1N0'
```
{% endtab %}
{% endtabs %}

NOTE: If fileName is not provided in the param then image name will be considered as the uploaded image name, if passed in the params, then that will be the name of the image.

**Response**

{% tabs %}
{% tab title="200" %}
```json
FILE WILL BE LOADED
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
