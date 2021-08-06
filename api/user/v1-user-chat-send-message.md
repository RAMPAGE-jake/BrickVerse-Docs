# v1/user/chat/send-message

{% api-method method="post" host="https://api.brickverse.co" path="/v1/user/chat/send-message" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
his endpoint sends message.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="content" type="string" required=true %}
Chat Message
{% endapi-method-parameter %}

{% api-method-parameter name="chatId" type="number" required=true %}
Chat ID
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
Authorization Token of user
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Message Sent!
{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=304 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{"status": "content-too-long"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
Non Opertional
{% endhint %}

