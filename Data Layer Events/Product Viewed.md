# Product Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Viewed",
    "product": [
        {
            "price": {
                "priceType": "<priceType>",
                "sellingPrice": "<sellingPrice>"
            },
            "productInfo": {
                "brand": "<brand>",
                "businessUnit": "<businessUnit>",
                "discountAmount": "<discountAmount>",
                "fulfillmentOptions": "<fulfillmentOptions>",
                "isOutOfStock": "<isOutOfStock>",
                "isSKuAvailable": "<isSKuAvailable>",
                "name": "<name>",
                "productID": "<productID>",
                "quantityAvailable": "<quantityAvailable>",
                "ratingAverage": "<ratingAverage>",
                "ratingCount": "<ratingCount>",
                "ratingCountAndAverageCombined": "<ratingCountAndAverageCombined>",
                "sku": "<sku>",
                "status": "<status>"
            }
        }
    ]
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|discountAmount|string|The product discount amount shown to the visitor for each product.|$20, 10%, $5|||||||
|fulfillmentOptions|string|The product fulfillment options available for each product to view impact on conversion.|Shipped Only, In Store Only, Local Pickup Only, In Store or Ship, Digital \(Email or Text\)|||||||
|isOutOfStock|boolean|Boolean flag indicating that an inventoried product is out of stock. |TRUE, FALSE|||||||
|isSKuAvailable|boolean|True\/False flag to indicate if product SKU is known at the time of the event|true, false|||||||
|priceType|string|Describes the type of price offered using commonly used terms. |1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|quantityAvailable|string|The product quantity available.|1, 10, 100|||||||
|ratingAverage|string|String representation of the average customer rating.  Positive. Up to two decimal places. This is most often a number between 0 and 5. |1.1, 2, 5|^[0-9]*(\.[0-9]{1,2})?$||||||
|ratingCount|integer|Integer number of customer ratings. |1, 5, 11, 200||||0|||
|ratingCountAndAverageCombined|string|Combined Rating Count and Rating Average with colon as delimiter|23:4.5, 222:1.7, 1:5, 2:3.5|||||||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|status|string|Described the product's status|In Stock, Out of Stcok, Back-Ordered|||||||



