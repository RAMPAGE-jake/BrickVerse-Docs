# v1/games/details

{% api-method method="post" host="https://api.brickverse.co" path="/v1/games/details" %}
{% api-method-summary %}
Game Information
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to see game details.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="target" type="number" required=true %}
Game ID
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
    "players": 30,
    "gameid": 12345,
    "gamename": "Adopt Me!"
    "owner": 1,
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
No results found in the database.
{% endapi-method-response-example-description %}

```
{"status": "error", "error" => "no data found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
Non-Operational as 6/30/2021 7:35 AM PDT. Under going changes
{% endhint %}

