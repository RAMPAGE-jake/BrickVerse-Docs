# v1/user/get-messages

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/chat/get-messages" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
This endpoint returns a table of the current messages
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="page" type="string" required=true %}
page id
{% endapi-method-parameter %}

{% api-method-parameter name="startId" type="string" required=true %}
start id
{% endapi-method-parameter %}

{% api-method-parameter name="chatId" type="number" required=true %}
ID Of Chat
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Authorization Token of user
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Summary Found
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
No results found in the database.
{% endapi-method-response-example-description %}

```
{"status": "error"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
Non Opertional, we're still drafting this backend up.
{% endhint %}



