# v1/render/avatar

{% swagger baseUrl="https://api.brickverse.co" path="/v1/render/avatar" method="post" summary="" %}
{% swagger-description %}
This endpoint allows you to create avatar renders
{% endswagger-description %}

{% swagger-parameter in="body" name="target" type="number" %}
UserId of the user
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
headshot or body (Type of render)
{% endswagger-parameter %}

{% swagger-response status="200" description="Render Generated" %}
```
{
    "status": "success",
    "userid": 1,
    "username:" "BrickVerse",
    "avatar": "https://cdn.brickverse.co/avatars/abcdefg123467890.png"
}
```
{% endswagger-response %}

{% swagger-response status="304" description="No user found" %}
```
{"status": "error", "error" => "User doesn't exist"}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="danger" %}
Non-Operational as 6/29/2021 11:06 PM PDT. Under going changes.&#x20;
{% endhint %}

{% hint style="warning" %}
Addtional API Cooldown is added blocking renders to only be created every 5 minutes (BrickVerse backend is exempt from this) to prevent over-loading the API with creating mass amount of renders.\
\
If you want to request a avatar instead, please use v1/user/avatar to fetch a users avatar already rendered.
{% endhint %}
