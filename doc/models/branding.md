
# Branding

Brand identity information derived from executing on-page javascript.

*This model accepts additional fields of type unknown.*

## Structure

`Branding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `logo` | `string \| null \| undefined` | Optional | Primary logo URL if detected. |
| `fonts` | [`Font[] \| undefined`](../../doc/models/font.md) | Optional | Detected font families. |
| `colors` | `unknown \| undefined` | Optional | - |
| `typography` | `unknown \| undefined` | Optional | - |
| `spacing` | `unknown \| undefined` | Optional | - |
| `components` | `unknown \| undefined` | Optional | - |
| `icons` | `unknown \| undefined` | Optional | - |
| `images` | `unknown \| undefined` | Optional | - |
| `animations` | `unknown \| undefined` | Optional | - |
| `layout` | `unknown \| undefined` | Optional | - |
| `tone` | `unknown \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Branding } from 'firecrawl-apilib';

const branding: Branding = {
  logo: 'logo0',
  fonts: [
    {
      family: 'family2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  colors: { 'key1': 'val1', 'key2': 'val2' },
  typography: { 'key1': 'val1', 'key2': 'val2' },
  spacing: { 'key1': 'val1', 'key2': 'val2' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

