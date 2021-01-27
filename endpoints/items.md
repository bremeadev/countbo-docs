# Items

{% api-method method="get" host="https://bremea.com" path="/api/countbot/items" %}
{% api-method-summary %}
Get All Items
{% endapi-method-summary %}

{% api-method-description %}
Returns all items including beta, disabled and discontinued items.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="type" type="string" required=false %}
An item type e.g. powerups or curses
{% endapi-method-parameter %}

{% api-method-parameter name="subtype" type="string" required=false %}
An item subtype e.g. skip or lose
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
All items are returned in an array.
{% endapi-method-response-example-description %}

```
[
  {
    "id": 1,
    "itemid": "p-s2",
    "name": "Skip 2",
    "type": "powerup",
    "subtype": "skip",
    "rarity": 100,
    "value": 2,
    "cost" :9,
    "emoji": ":fast_forward:",
    "description": "Adds 2 to the current count in a counting channel.",
    "icon": "https://raw.githubusercontent.com/twitter/twemoji/master/assets/svg/23e9.svg",
    "emojicode": "23e9",
    "discount":{"active":false},
    "altcost": 9
  },
  
  ...
  
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bremea.com" path="/api/countbot/items/:id" %}
{% api-method-summary %}
Get Specific Item
{% endapi-method-summary %}

{% api-method-description %}
Returns information of the provided item ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
An item's ID e.g. p-s2
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Item was successfully found.
{% endapi-method-response-example-description %}

```
{
  "id": 1,
  "itemid": "p-s2",
  "name": "Skip 2",
  "type": "powerup",
  "subtype": "skip",
  "rarity": 100, 
  "value": 2,
  "cost": 9,
  "emoji": ":fast_forward:",
  "description": "Adds 2 to the current count in a counting channel.",
  "icon": "https://raw.githubusercontent.com/twitter/twemoji/master/assets/svg/23e9.svg",
  "emojicode": "23e9",
  "discount": {
    "active": false
  },
  "altcost": 9
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Invalid item ID provided
{% endapi-method-response-example-description %}

```
{
  "error": true,
  "code": 404,
  "msg": "Item not found.",
  "discount": {
    "active": false
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

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
{% api-method-parameter name="amount" type="number" %}
The number of random items to return, default 1
{% endapi-method-parameter %}

{% api-method-parameter name="nocurses" type="boolean" required=false %}
Whether or not to include curses in the response
{% endapi-method-parameter %}

{% api-method-parameter name="nopowerups" type="boolean" required=false %}
Whether or not to include powerups in the response
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

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

