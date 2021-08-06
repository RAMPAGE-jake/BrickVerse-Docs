# v1/render/avatar

{% api-method method="post" host="https://api.brickverse.co" path="/v1/render/avatar" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create avatar renders
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="target" type="number" required=true %}
UserId of the user
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
headshot or body \(Type of render\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Render Generated
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "userid": 1,
    "username:" "BrickVerse",
    "avatar": "https://cdn.brickverse.co/avatars/abcdefg123467890.png"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=304 %}
{% api-method-response-example-description %}
No user found
{% endapi-method-response-example-description %}

```
{"status": "error", "error" => "User doesn't exist"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
Non-Operational as 6/29/2021 11:06 PM PDT. Under going changes. 
{% endhint %}

{% hint style="warning" %}
Addtional API Cooldown is added blocking renders to only be created every 5 minutes \(BrickVerse backend is exempt from this\) to prevent over-loading the API with creating mass amount of renders.  
  
If you want to request a avatar instead, please use v1/user/avatar to fetch a users avatar already rendered.
{% endhint %}

