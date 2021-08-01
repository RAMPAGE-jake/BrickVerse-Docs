# v1/user/friend

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/friend" %}
{% api-method-summary %}
Add Friend
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create friend requests.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
API Token, go to brickverse.co/user/settings/api for one.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="friend" type="number" required=true %}
UserId of sender
{% endapi-method-parameter %}

{% api-method-parameter name="target" type="number" required=true %}
UserId of target to add
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Request Created
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "message": "sent"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}
Already Friends
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "message": "active friends"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=304 %}
{% api-method-response-example-description %}
Active Request
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "message": "active request"
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

{% hint style="success" %}
Function Operational as 6/28/2021 2:44 AM PDT
{% endhint %}

