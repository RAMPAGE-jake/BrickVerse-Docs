# username-available

{% swagger method="get" path="/username-available" baseUrl="https://api.brickverse.co/v2/user" summary="Information" %}
{% swagger-description %}
API used to chec avaliablity of a username on registration & username changes.

\




\


Username field must be passed as a query (?username=foo) or body param ({"username":"foo"}).
{% endswagger-description %}

{% swagger-parameter in="body" required="true" name="username" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="query" name="username" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Response" %}
```json
{"status": "ok", "available": boolean}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}
```json
{"status": "error"}
```
{% endswagger-response %}

{% swagger-response status="429: Too Many Requests" description="" %}
```json
{"status": "error", "message": "Rate limited", "ratelimited": true, "time": "seconds_string"}
```
{% endswagger-response %}
{% endswagger %}
