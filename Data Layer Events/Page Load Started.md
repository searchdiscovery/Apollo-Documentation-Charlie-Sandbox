# Page Load Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "page_view",
  "apollo_event": "Page Load Started",
    "page": {
        "pageName": "<pageName>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||




