# Item Resources

    POST quotations

## Description
Returns a list of quotations.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
- **fromLocale** _(required)_ - the locale to be translated from, default base locale of the project
- **toLocales** _(required)_ — locale ids to be translated to, comma separated, refer to [GET locales](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/locale/GET_locales.md)
- **strings** _(required)_ - strings to be translated, a simple array

***

## Return format
An array with the following keys and values:

- **quotations** — A set of quotations available.

***

## Errors
None

***

## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:projectId/quotations

**Return** __shortened for example purpose__
``` json
{
    "quotations": [
        {
            "id": 123,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Japanese",
            "toLocale": "jp",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "estimatedReturnDatetime": "2013-01-01 23:00:00 GMT+0",
            "estimatedReturnTimestamp": 13453435132,
            "estimatedSecondsFromNow": 1234567
        },
        {
            "id": 122,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Korean",
            "toLocale": "ko",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "estimatedReturnDatetime": "2013-01-01 23:00:00 GMT+0",
            "estimatedReturnTimestamp": 13453435132,
            "estimatedSecondsFromNow": 1234567
        }
    ]
}
```