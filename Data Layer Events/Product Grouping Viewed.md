# Product Grouping Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Grouping Viewed",
    "productGrouping": {
        "level1": "<level1>",
        "level2": "<level2>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|level1|string|The top level product grouping associated with the page that is currently being viewed.|men's clothing, women's clothing|||||||
|level2|string|The second level product grouping associated with the page that is currently being viewed.|shirts, shoes|||||||



