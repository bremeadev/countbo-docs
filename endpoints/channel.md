# Channel

{% api-method method="get" host="https://bremea.com" path="/api/countbot/channel/:id" %}
{% api-method-summary %}
Get Counting Channel Information
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
Counting Channel ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Counting Channel information is returned.
{% endapi-method-response-example-description %}

```
{
  "id": 47,
  "guildid": "727721043283935252",
  "channelid": "728826784187154483",
  "goal": 20000,
  "milestones": true,
  "finished": false,
  "powerups": true,
  "curses": true,
  "userlimit": false,
  "sudo": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
No Counting Channel with the provided ID was found.
{% endapi-method-response-example-description %}

```
{
  "error": true,
  "code": 404,
  "msg": "Channel does not exist."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bremea.com" path="/api/countbot/channel/:id" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
No channel was found matching the provided ID.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



