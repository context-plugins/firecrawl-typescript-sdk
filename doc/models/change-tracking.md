
# Change Tracking

Change tracking information if `changeTracking` is in `formats`. Only present when the `changeTracking` format is requested.

*This model accepts additional fields of type unknown.*

## Structure

`ChangeTracking`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `previousScrapeAt` | `string \| null \| undefined` | Optional | The timestamp of the previous scrape that the current page is being compared against. Null if no previous scrape exists. |
| `changeStatus` | [`ChangeStatus \| undefined`](../../doc/models/change-status.md) | Optional | The result of the comparison between the two page versions. 'new' means this page did not exist before, 'same' means content has not changed, 'changed' means content has changed, 'removed' means the page was removed. |
| `visibility` | [`Visibility \| undefined`](../../doc/models/visibility.md) | Optional | The visibility of the current page/URL. 'visible' means the URL was discovered through an organic route (links or sitemap), 'hidden' means the URL was discovered through memory from previous crawls. |
| `diff` | `string \| null \| undefined` | Optional | Git-style diff of changes when using 'git-diff' mode. Only present when the mode is set to 'git-diff'. |
| `json` | `unknown \| null \| undefined` | Optional | JSON comparison results when using 'json' mode. Only present when the mode is set to 'json'. This will emit a list of all the keys and their values from the `previous` and `current` scrapes based on the type defined in the `schema`. Example [here](/features/change-tracking) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ChangeStatus, ChangeTracking, Visibility } from 'firecrawl-apilib';

const changeTracking: ChangeTracking = {
  previousScrapeAt: '2016-03-13T12:52:32.123Z',
  changeStatus: ChangeStatus.New,
  visibility: Visibility.Visible,
  diff: 'diff8',
  json: { 'key1': 'val1', 'key2': 'val2' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

