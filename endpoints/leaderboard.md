# Leaderboard

{% api-method method="get" host="https://bremea.com" path="/api/countbot/leaderboard/:id" %}
{% api-method-summary %}
Get Guild Leaderboard
{% endapi-method-summary %}

{% api-method-description %}
This endpoint returns the leaderboard of the provided Discord Server ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
A Discord Server ID e.g. 727721043283935252
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Leaderboard successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "global": [
    {
      "discordid": "274014973401890816",
      "username": "Mitinho#5279",
      "xp": 51745
    },
    {
      "discordid": "683869330223530074",
      "username": "bremea#8975",
      "xp": 42484
    },
    {
      "discordid": "598560018014535697",
      "username": "Adro#0357",
      "xp": 17616
    },
    {
      "discordid": "694984504191877220",
      "username": "lxene#5433",
      "xp": 13833
    },
    {
      "discordid": "553089103747481604",
      "username": "Charly#6070",
      "xp": 12796
    }
  ],
  "727721043283935252": [
    {
      "discordid": "683869330223530074",
      "username": "bremea#8975",
      "xp": 3078
    },
    {
      "discordid": "476128837613387776",
      "username": "leilanibecool#4120",
      "xp": 862
    },
    {
      "discordid": "589044704708919316",
      "username": "decc00n#6684",
      "xp": 540
    },
    {
      "discordid": "694984504191877220",
      "username": "lxene#5433",
      "xp": 480
    },
    {
      "discordid": "534845467671003147",
      "username": "Migeul55#6350",
      "xp": 450
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bremea.com" path="/api/countbot/leaderboard" %}
{% api-method-summary %}
Get Global Leaderboard
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "global": [
    {
      "discordid": "597198645892218900",
      "username": "Carpincho#6666",
      "xp": 1219633,
      "mainbadge": ":rainbow_flag:"
    },
    {
      "discordid": "689970824257863691",
      "username": "Coliflor#2824",
      "xp": 328146,
      "mainbadge": ":rainbow_flag:"
    },
    {
      "discordid": "683869330223530074",
      "username": "bremea#8975",
      "xp": 279713,
      "mainbadge": ":ballot_box:"
    },
    {
      "discordid": "439618398410768385",
      "username": "People98765#2355",
      "xp": 74792,
      "mainbadge": ":fast_forward:"
    },
    {
      "discordid": "689581633095073817",
      "username": "Joker2007#0079",
      "xp": 55158,
      "mainbadge": ":christmas_tree:"
    }
  ],
  "christmas": {
    "discordid": "689581633095073817",
    "username": "Joker2007#0079",
    "trees": 742,
    "mainbadge": ":christmas_tree:"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

