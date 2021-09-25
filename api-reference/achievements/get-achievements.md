# GET Achievements

{% api-method method="get" host="https://achievements.xboxlive.com" path="/users/:userId/achievements" %}
{% api-method-summary %}
Get Achievements
{% endapi-method-summary %}

{% api-method-description %}
Gets the user's or users achievements
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userID" type="string" required=true %}
Can only be 'xuid\(12345\)'
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
XBL3.0 Token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="unlockedOnly" type="boolean" required=false %}
Will only show achievements that have been unlocked or in progress. Can only be 'true' or 'false'.
{% endapi-method-parameter %}

{% api-method-parameter name="skipItems" type="integer" required=false %}
The amount of items/achievements that can be skipped from the top.
{% endapi-method-parameter %}

{% api-method-parameter name="maxItems" type="integer" required=false %}
The maximum amount of items that can be received.
{% endapi-method-parameter %}

{% api-method-parameter name="orderBy" type="string" required=false %}
Priorities achievements from top to bottom.
{% endapi-method-parameter %}

{% api-method-parameter name="titleId" type="integer" required=false %}
A Title ID that grabs achievement through that title. Example: 950328474
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "achievements": [
    {
      "id": "4",
      "serviceConfigId": "00000000-0000-0000-0000-0000765b6743",
      "name": "Snow Problem",
      "titleAssociations": [
        {
          "name": "Forza Horizon 4",
          "id": 1985701699
        }
      ],
      "progressState": "Achieved",
      "progression": {
        "requirements": [],
        "timeUnlocked": "2019-08-31T16:55:37.1630000Z"
      },
      "mediaAssets": [
        {
          "name": "e5bb65b8-29c1-40f5-aec4-e6a37b1bbe99",
          "type": "Icon",
          "url": "http://images-eds.xboxlive.com/image?url=27S1DHqE.cHkmFg4nspsdw9P3IipOaQBSLBdmrcHoit37j9kEgXtrFGVbQFCZKvbyNhkSlF191P9IDSjNAoNh0PAYiUGo_deFnlXFhmXCaJk1H0Kkw4cuZrbARM6QOsh"
        }
      ],
      "platforms": [
        "XboxOne"
      ],
      "isSecret": false,
      "description": "Qualify for Horizon Winter.",
      "lockedDescription": "Qualify for Horizon Winter.",
      "productId": "00000000-0000-0000-0000-0000765b6743",
      "achievementType": "Persistent",
      "participationType": "Individual",
      "timeWindow": null,
      "rewards": [
        {
          "name": null,
          "description": null,
          "value": "10",
          "type": "Gamerscore",
          "mediaAsset": null,
          "valueType": "Int"
        }
      ],
      "estimatedTime": "00:00:00",
      "deeplink": "",
      "isRevoked": false,
      "rarity": {
        "currentCategory": "Common",
        "currentPercentage": 50.14
      }
    }
  ],
  "pagingInfo": {
    "totalRecords": 1138
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
# Types of orders

[
    'Default',
    'MostRare',
    'EndingSoon',
    'titleId',
]
```

