# v1/user/avatar

{% swagger baseUrl="https://api.brickverse.co" path="/v1/user/avatar" method="post" summary="Search Users" %}
{% swagger-description %}
This endpoint allows you to get avtar URL of an user, this doesn't generate a render.
{% endswagger-description %}

{% swagger-parameter in="body" name="target" type="string" %}
Full Username Or UserID
{% endswagger-parameter %}

{% swagger-response status="200" description="User Found" %}
```
{
    "status": "success",
    "avatar": "https://cdn.brickverse.co/avatars/example.png"
}
```
{% endswagger-response %}

{% swagger-response status="404" description="No results found in the database." %}
```
{"status": "error", "error" => "no results"}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="danger" %}
API Under going changes, non-functional.
{% endhint %}
