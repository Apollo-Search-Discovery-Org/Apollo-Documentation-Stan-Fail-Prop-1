# Onsite Search Performed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Onsite Search Performed",
    "onsiteSearch": {
        "keyword": {
            "searchTerm": "<searchTerm>",
            "searchTermCorrected": "<searchTermCorrected>",
            "searchType": "<searchType>"
        },
        "location": {
            "center": {
                "accuracy": "<accuracy>",
                "latitude": "<latitude>",
                "longitude": "<longitude>"
            },
            "map": {
                "vendor": "<vendor>",
                "zoomLevel": "<zoomLevel>"
            },
            "radius": {
                "unitOfMeasure": "<unitOfMeasure>",
                "value": "<value>"
            }
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|accuracy|string|A representation of the accuracy of the method that provides the location center.|high, medium, low|||||||
|latitude|number|The latitude of the map center for a property search.|48.858093||||-90|90||
|longitude|number|The longitude of the map center for a property search.|2.294694||||-180|180||
|searchTerm|string|Describes the search keyword used after auto-correct, auto-complete, or keyword suggestion. |bluth, blue, red lobster|||||||
|searchTermCorrected|string|Describes the search keyword exactly as entered by the user before any auto-correct or auto complete actions take place.  This is the search term that was corrected. |bluth:blu, blue:blu, red lobster:rd lbstr|||||||
|searchType|string|Describes the domain of the search. |products, properties, articles, authors, coupons, publications|||||||
|unitOfMeasure|string|The unit of measurement|miles, kilometers, meters|||||||
|value|number|The location search radius from the center POI.|2.294694||||0|||
|vendor|string|The technology vendor of the map|Google, Bing, Mapquest, ESRI|||||||
|zoomLevel|string|Indicator of the zoom level in a map presentation. Values are typically integers, but can vary depending on the map service used. |1, 2, 3, 4, 5, 6|||||||



