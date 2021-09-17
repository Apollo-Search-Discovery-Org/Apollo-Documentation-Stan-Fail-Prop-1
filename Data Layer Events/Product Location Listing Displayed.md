# Product Location Listing Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Location Listing Displayed",
    "listingDisplayed": {
        "displayCount": "<displayCount>",
        "filterList": "<filterList>",
        "filterListLength": "<filterListLength>",
        "listing": [
            {
                "isDisplayed": "<isDisplayed>",
                "itemPosition": "<itemPosition>",
                "location": {
                    "latitude": "<latitude>",
                    "locationBrand": "<locationBrand>",
                    "locationDistanceFromPOI": "<locationDistanceFromPOI>",
                    "locationId": "<locationId>",
                    "locationName": "<locationName>",
                    "locationStatus": "<locationStatus>",
                    "locationType": "<locationType>",
                    "longitude": "<longitude>"
                },
                "price": {
                    "currency": "<currency>"
                },
                "productInfo": {
                    "sku": "<sku>"
                }
            }
        ],
        "listingDriver": "<listingDriver>",
        "listingType": "<listingType>",
        "resultsCount": "<resultsCount>",
        "sortDefault": "<sortDefault>",
        "sortOrder": "<sortOrder>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|currency|string|Currency of the prices given. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|displayCount|integer|The total number of items displayed out of all returned items. \(Integer\)|10, 20, 30, 40||||0|||
|filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||
|filterListLength|integer|The number of filterValue pairs in the filterList|0, 20, 12||||0|||
|isDisplayed|boolean|Helper node used by AA Product String Builder to set product scoped events|true|||||||
|itemPosition|integer|Integer position of a property within a sorted result. The first returned is position 1. For map results, this value can be the rank by distance from POI.|1, 2, 3, 4, 5||||0|||
|latitude|number|The latitude of the map center for a location search.|48.858093||||-90|90||
|listingDriver|string|Describes the action that caused the listing to be displayed|Onsite Search, Curated Assortment, Navigation|||||||
|listingType|string|The type of results being listed|text, product, location, event, room, product location|||||||
|locationBrand|string|The brand associated with a location.|BMO Harris, Walmart, Lands' End, Motel 6, AC Hotels|||||||
|locationDistanceFromPOI|integer|The distance from the location to the user's point of interest|12, 3, 5, 200|||||||
|locationId|string|Unique Identifier of a Location. |155, 65588, 987764448|||||||
|locationName|string|The friendly name of the location.|Deerefiled Outlet, Old Orchard, Manhatten Midtown|||||||
|locationStatus|string|The status of a location.|Closed, Open, Coming Soon, Wait-listed|||||||
|locationType|string|The type of the location|Retail Store, Lodging, ATM, Banking Branch|||||||
|longitude|number|The longitude of the map center for a location search.|2.294694||||-180|180||
|resultsCount|integer|The total number of items returned that matched the search criteria. \(Integer\)|1, 21, 111, 166||||0|||
|sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|sortDefault|integer|The default sort value on listings|A to Z, Low to High, Newest to Oldest||||0|||
|sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||



