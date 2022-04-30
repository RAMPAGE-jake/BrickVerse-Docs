# v1/user/get-by-username

{% swagger baseUrl="https://api.brickverse.co" path="/v1/user/get-by-username" method="post" summary="Search Users" %}
{% swagger-description %}
Get a user by username.
{% endswagger-description %}

{% swagger-parameter in="query" name="username" required="true" type="String" %}
Player Username
{% endswagger-parameter %}

{% swagger-response status="200" description="User Found" %}
```
{
    "status": "success",
    "username": "ArkInfinity",
    "id": 3
}
```
{% endswagger-response %}

{% swagger-response status="404" description="No results found in the database." %}
```
{"status": "failed", "reason" => "no results"}
```
{% endswagger-response %}
{% endswagger %}

## Errors

|           Error          |            Fix           |
| :----------------------: | :----------------------: |
| Username wasn't found. 1 | No username found in GET |
| Username wasn't found. 2 |    No database results   |
