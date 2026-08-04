
# Batch Scrape Request Actions

## Class Name

`BatchScrapeRequestActions`

## Cases

| Type |
|  --- |
| [`Wait`](../../../doc/models/wait.md) |
| [`Screenshot`](../../../doc/models/screenshot.md) |
| [`Click`](../../../doc/models/click.md) |
| [`WriteText`](../../../doc/models/write-text.md) |
| [`PressAKey`](../../../doc/models/press-a-key.md) |
| [`Scroll`](../../../doc/models/scroll.md) |
| [`Scrape`](../../../doc/models/scrape.md) |
| [`ExecuteJavaScript`](../../../doc/models/execute-java-script.md) |

## Wait

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type.Wait,
  selector: '#my-element',
};
```

## Screenshot

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type1.Screenshot,
  fullPage: false,
};
```

## Click

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type2.Click,
  selector: '#load-more-button',
  all: false,
};
```

## WriteText

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type3.Write,
  text: 'Hello, world!',
};
```

## PressAKey

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type4.Press,
  key: 'Enter',
};
```

## Scroll

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type5.Scroll,
  direction: Direction.Down,
  selector: '#my-element',
};
```

## Scrape

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type6.Scrape,
};
```

## ExecuteJavaScript

### Initialization Code

#### Example

```ts
const value: BatchScrapeRequestActions = {
  type: Type7.ExecuteJavascript,
  script: 'document.querySelector(\'.button\').click();',
};
```

