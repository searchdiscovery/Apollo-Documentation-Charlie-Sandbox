# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "purchase",
  "apollo_event": "Order Placed",
    "cart": {
        "cartID": "<cartID>"
    },
    "transaction": {
        "item": [
            {
                "price": {
                    "basePrice": "<basePrice>",
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "brand": "<brand>",
                    "businessUnit": "<businessUnit>",
                    "productID": "<productID>"
                },
                "quantity": <quantity>,
                "voucherDiscount": {
                    "orderLevelDiscountAmount": "<orderLevelDiscountAmount>",
                    "orderLevelDiscountCode": "<orderLevelDiscountCode>",
                    "productLevelDiscountCode": "<productLevelDiscountCode>"
                }
            }
        ],
        "payment": [
            {
                "paymentAmount": "<paymentAmount>",
                "paymentGateway": "<paymentGateway>",
                "paymentID": "<paymentID>",
                "paymentMethod": "<paymentMethod>"
            }
        ],
        "profile": {
            "address": {
                "country": "<country>",
                "postalCode": "<postalCode>",
                "stateProvince": "<stateProvince>"
            }
        },
        "purchaseID": "<purchaseID>",
        "total": {
            "currency": "<currency>",
            "revenue": "<revenue>"
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|basePrice|string|String representation of MSRP of a product. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|country|string|Indicates the country of the billing address. ISO 3166 \(alpha-2\) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|orderLevelDiscountAmount|string|String representation of an order level discount applied to an item in a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|orderLevelDiscountCode|string|Order Level Discount code applied at the item level of a transaction. |FRIENDSANDFAMILY20, EASTER10|||||||
|paymentAmount|string|String representation of the payment amount. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|paymentGateway|string|Captures the digital payment gateway was used to complete transactions for orders?|PayPal, Stripe|||||||
|paymentID|string|Unique identifier of a payment.  Typically an integration key from a back-end system.|ZPH-87698-098|||||||
|paymentMethod|string|Describes the method of payment for a transaction. |Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|postalCode|string|The mailing zip or postal code associated with the billing address. |53533, 30381, M1R 0E9, M3C 0C1|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|productLevelDiscountCode|string|Discount code applied for a specific item \(or items\) of a transaction. |5OFFSHOES, AKRONCANDLES2019|||||||
|purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|revenue|string|The total revenue for a transaction. Does not include tax or shipping. |125.05, 432.21, 90.22, 12.05|^[0-9]*(\.[0-9]{1,2})?$||||||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|stateProvince|string|The mailing state or province associated with billing address. |WI, GA, NB, ON|||||||




