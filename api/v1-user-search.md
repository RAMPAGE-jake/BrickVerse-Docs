# v1/user/search

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/search" %}
{% api-method-summary %}
Search Users
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to search for users in the BrickVerse Database.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token. For public usage use token "public"
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
Part of or full username of player.
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
    "data": [{
        "username": "ArkInfinity",
        "id": "4",
        "avatar_url": "https:\/\/brickverse.co\/assets\/img\/male.png"
    }]
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

