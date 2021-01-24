# Stats

{% api-method method="get" host="https://bremea.com" path="/api/countbot/stats/:id" %}
{% api-method-summary %}
Get User Stats
{% endapi-method-summary %}

{% api-method-description %}
This endpoint returns statistics for specific users.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
User's Discord ID e.g. 727569067895947383
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="channelid" type="string" %}
Specific counting channel versus all channels the user is a part of
{% endapi-method-parameter %}

{% api-method-parameter name="guildid" type="string" %}
Specific server ID to return all channels the user is in for that guild
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "coins": 1205060,
  "counted": 46,
  "powerups": 1,
  "curses": 2,
  "xp": 172,
  "votes": 0,
  "bought": 5,
  "booster": 1,
  "longeststreak": 24,
  "level": 5,
  "plvls": 160,
  "lvls": 320,
  "guilds": {
    "727721043283935252": {
      "coins": 1205060,
      "counted": 46,
      "powerups": 1,
      "curses": 2,
      "xp": 172,
      "votes": 0,
      "bought": 5,
      "booster": 1,
      "longeststreak": 24
    }
  },
  "channels": {
    "728826784187154483": {
      "id": 6828,
      "discordid": "353242705545134090",
      "username": "",
      "guildid": "727721043283935252",
      "channelid": "728826784187154483",
      "counted": 0,
      "powerups": 0,
      "curses": 0,
      "votes": 0,
      "streak": 0,
      "longeststreak": 0,
      "coins": 5000,
      "bought": 0,
      "xp": 0,
      "level": 0,
      "multiplier": 1,
      "multiend": "2020-11-01T22:35:44.000Z"
    }
  },
  "code": 200
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a user matching the provided user ID.
{% endapi-method-response-example-description %}

```
{
  "error": true,
  "code": 404,
  "msg": "User does not exist"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



