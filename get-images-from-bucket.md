# Get Images from bucket

## This api helps inserting images in the bucket

<mark style="color:green;">`GET`</mark> api/buckets/\<bucketname>/objects/\<filename>

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
