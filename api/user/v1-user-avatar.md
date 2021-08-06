# v1/user/avatar

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/avatar" %}
{% api-method-summary %}
Search Users
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get avtar URL of an user, this doesn't generate a render.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="target" type="string" required=true %}
Full Username Or UserID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User Found
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "avatar": "https://cdn.brickverse.co/avatars/example.png"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
No results found in the database.
{% endapi-method-response-example-description %}

```
{"status": "error", "error" => "no results"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
API Under going changes, non-functional.
{% endhint %}

