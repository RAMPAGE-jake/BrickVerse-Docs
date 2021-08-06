# v1/user/chat/chats

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/chat/chats" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
This endpoint returns a table of past user has been chatting with for the Chat Widget.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Authorization Token of user
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
        "avatar_url": "https:\/\/brickverse.co\/assets\/img\/male.png",
        "last_message": "hello world",
        "chat_id": "1",
        "chat_name": "epic friends chat!"
    }]
}
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
Non Opertional
{% endhint %}

