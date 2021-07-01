# v1/user/friends

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/friends" %}
{% api-method-summary %}
View Friends
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to see active-friends.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="target" type="number" required=true %}
UserId of the user
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
        "username": "nate",
        "id": "6",
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
{"status": "error", "error" => "User has no friends"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="success" %}
Operational as 6/28/2021 2:44 AM PDT. Under going changes
{% endhint %}

