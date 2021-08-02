# v1/get

{% api-method method="post" host="https://api.brickverse.co" path="/v1/asset/get" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get asset information
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="assetid" type="number" required=true %}
AssetID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Friends Found!
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "data": [{
        "id": "1",
        "name": "Baseplate",
        "type": "Universe",
        "creator": "1",
    }]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
No results found in the database.
{% endapi-method-response-example-description %}

```
{"status": "error", "error" => "No asset could be found with that ID"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="success" %}
Operational as 8/1/2021 8:57 PM PDT.
{% endhint %}

