# Random Items

{% api-method method="get" host="https://bremea.com" path="/api/countbot/randomitems" %}
{% api-method-summary %}
Get Random Items
{% endapi-method-summary %}

{% api-method-description %}
This endpoint returns random items.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="amount" type="number" required=false %}
A number of random items to return, default 1
{% endapi-method-parameter %}

{% api-method-parameter name="nocurses" type="boolean" %}
Whether or not to include curses in the response
{% endapi-method-parameter %}

{% api-method-parameter name="nopowerups" type="boolean" %}
Whether or not to include powerups in the response
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Random tems successfully retrieved.
{% endapi-method-response-example-description %}

```
[
  {
    "id": 17,
    "itemid": "c-l10",
    "name": "Lose 10",
    "type": "curse",
    "subtype": "lose",
    "rarity": 80,
    "value": 10,
    "cost": 20,
    "emoji": ":rewind:"
  },
  {
    "id": 16,
    "itemid": "c-l5",
    "name": "Lose 5",
    "type": "curse",
    "subtype": "lose",
    "rarity": 99,
    "value": 5,
    "cost": 10,
    "emoji": ":rewind:"
  },
  {
    "id": 15,
    "itemid": "c-l2",
    "name": "Lose 2",
    "type": "curse",
    "subtype": "lose",
    "rarity": 100,
    "value": 2,
    "cost": 4,
    "emoji": ":rewind:"
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
An invalid number of items to return was provided
{% endapi-method-response-example-description %}

```
{
  "error": true,
  "code": 400,
  "msg": "Provided number was too large."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



