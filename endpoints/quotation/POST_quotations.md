# Quotation Resources

    POST quotations

## Description
Returns a list of quotations.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `from_locale` _(required)_ - the locale to be translated from, default base locale of the project
- `to_locales` _(required)_ - locale ids to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - strings to be translated, format reference [here](/reference/formats.md#items)
- `is_including_review` _(optional)_ - if need to include 1 more reviewer, `1` or `0`, default `0`

## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/quotations

**Response**
``` json
{
    "quotations": [
        {
            "id": 123,
            "from_language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            },
            "to_language": {
                "code": "ja-JP",
                "english_name": "Japanese",
                "local_name": "日本語",
                "locale": "ja",
                "region" : "JP"
            },
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_datetime": "2013-01-01T23:00:00+0000",
            "estimated_return_timestamp": 13453435132,
            "estimated_seconds_from_now": 1234567
        },
        {
            "id": 122,
            "from_language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            },
            "to_language": {
                "code": "ko-KR",
                "english_name": "Korean",
                "local_name": "한국어",
                "locale": "ko",
                "region" : "KR"
            },
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_datetime": "2013-01-01T23:00:00+0000",
            "estimated_return_timestamp": 13453435132,
            "estimated_seconds_from_now": 1234567
        }
    ]
}
```
