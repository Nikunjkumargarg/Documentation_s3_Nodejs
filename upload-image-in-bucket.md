# Upload Image In Bucket

## This api helps inserting images in the bucket

<mark style="color:green;">`POST`</mark> /api/bucket/\<bucketName>/objects\
<mark style="color:green;">`POST`</mark> /api/bucket/\<bucketName>/objects/\<fileName>

{% tabs %}
{% tab title="CURL" %}
```javascript
curl --location 'http://localhost:3000/api/bucket/JKTECHNOLOGY/objects/' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6Im5pa3VuaiIsInVzZXJpZCI6IjFjOGMwN2I4LTg4ZTMtNDg0NC05MTFlLThmMWFlZjg5Yjg4NiIsImlhdCI6MTcyMTYyNzQwOCwiZXhwIjoxNzIyMjMyMjA4fQ.xKYkkC-4ooPz62in1Xx7v6lbxhNOl6j0jDhFt5KM7EY' \
--form 'file=@"/C:/Users/nikun/Downloads/COMMON RECRUITMENT PROCESS FOR RECRUITMENT OF CLERKS IN PARTICIPATING BANKS (CRP CLERKS-XIV).pdf"'
```
{% endtab %}
{% endtabs %}

NOTE: If fileName is not provided in the param then file name will be considered as the uploaded file name, if passed in the params, then that will be the name of the file.

**Body**

| Key  | Type | Description              | Required |
| ---- | ---- | ------------------------ | -------- |
| file | File | upload image of any type | Yes      |

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "message": "File uploaded successfully"
}
```
{% endtab %}

{% tab title="400" %}
```json
{
    "error": "No file uploaded or file is empty."
}
```
{% endtab %}
{% endtabs %}
