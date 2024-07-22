# Upload Image In Bucket

## This api helps inserting images in the bucket

<mark style="color:green;">`POST`</mark> /api/buckets/\<bucketName>/objects\
<mark style="color:green;">`POST`</mark> /api/buckets/\<bucketName>/objects/\<fileName>

NOTE: If fileName is not provided in the param then image name will be considered as the uploaded image name, if passed in the params, then that will be the name of the image.

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
