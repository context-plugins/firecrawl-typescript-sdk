
# Location

Location settings for the request. When specified, this will use an appropriate proxy if available and emulate the corresponding language and timezone settings. Defaults to 'US' if not specified.

*This model accepts additional fields of type unknown.*

## Structure

`Location`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `country` | `string \| undefined` | Optional | ISO 3166-1 alpha-2 country code (e.g., 'US', 'AU', 'DE', 'JP')<br><br>**Default**: `'US'`<br><br>**Constraints**: *Pattern*: `^[A-Z]{2}$` |
| `languages` | `string[] \| undefined` | Optional | Preferred languages and locales for the request in order of priority. Defaults to the language of the specified location. See https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Language |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Location } from 'firecrawl-apilib';

const location: Location = {
  country: 'US',
  languages: [
    'languages3',
    'languages2'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

