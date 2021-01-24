# Guild Channel

{% api-method method="get" host="https://bremea.com" path="/api/countbot/guild/:id" %}
{% api-method-summary %}
Get Guild's Counting Channels
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
A Discord Server ID e.g. 727721043283935252
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "anotherchannel": true,
  "channelid": "728826784187154483"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Invalid guild ID provided
{% endapi-method-response-example-description %}

```
{
  "error": true,
  "code": 404,
  "msg": "Guild does not exist"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



