## Widgets

Ensure you select the widget type corresponding to whether you are a **'Little things'** seller or a **'Big Things'** seller.


You will need to insert the script where you want the widget to display (typically directly below the product price), replacing the <code>PLACE_YOUR_PRODUCT_PRICE</code> field with the product's price parameter.


## 'Little things' Widget

If a **'Little things'** only seller, use:

```
<script src="https://widgets.%domain%/content/scripts/price-info.js?productPrice=PLACE_YOUR_PRODUCT_PRICE&little=f5"></script>
```
<script src="https://widgets.%domain%/content/scripts/price-info.js?productPrice=100&little=F5"></script>

## 'Big things' Dynamic API Pricing Widget

The **'Big things'** widget can display dynamic big things pricing tailored to the terms applied to your humm account.

``` 
<script src="https://widgets.%domain%/content/scripts/price-info.js?productPrice=PLACE_YOUR_PRODUCT_PRICE&BigThings&merchantId=YOUR_MERCHANT_ID"></script>
```

Note the use of the <code>&BigThings</code> and <code>&merchantId</code> parameters.

Replace the <code>YOUR_MERCHANT_ID</code> parameter in the above script with your merchant ID. 

<script
src="https://widgets.%domain%/content/scripts/price-info.js?productPrice=1500&BigThings&merchantId=30132859"></script>

## Platform-specific Installation Instructions
* [Shopify](/widgets/price-info/shopify_nz)
* [Magento 1](/widgets/price-info/magento_1_nz)
* [OpenCart 3](/widgets/price-info/opencart_3_nz)


## Dynamic Widget

Provide a ```price-selector``` query argument to target the HTML element containing the price. This will update the widget as the product price changes on user selection.

Provide a **URL encoded** jQuery CSS selector.

Here is HTML taken from a WooCommerce product page:

```
<span>Product Price:</span>
<p class="price">
    <span id="priceinfo" class="woocommerce-Price-amount amount">
        <span class="woocommerce-Price-currencySymbol">$</span>900.00
    </span>
</p>
```

<p class="price">
    <span><strong>Product Price</strong>:</span>
    <span id="priceinfo" class="woocommerce-Price-amount amount">
        <span class="woocommerce-Price-currencySymbol">$</span>900.00
    </span>
</p>

Use the urlencoded ```%23priceinfo ``` to reference the id ```#priceinfo```

<script src="https://widgets.%domain%/content/scripts/price-info.js?price-selector=%23priceinfo"></script>
```
<script src="https://widgets.%domain%/content/scripts/price-info.js?price-selector=%23priceinfo"></script>
```

You could also use ```price-selector=.woocommerce-Price-amount.amount``` or any CSS selector to identify the price.


## Minimum and Maximum Widgets

**'Little things'** and **'Big things'** widgets have default minimum and maximum thresholds.

You can customise the min and max threshold (can only increase the min or/and decrease the max) by setting ```data-min``` and ```data-max``` accordingly when calling the widget.

<p style=display:%nz-only%>
    By default, "Little things" shows when product price is between $20 and $1000, while "Big things" shows only between the price of $80 and $10000.
</p>
```
<script data-min="20" data-max="300" src="https://widgets.%domain%/content/scripts/price-info.js?productPrice=YOUR_PRICE"></script>
```

Here it will not display for prices above $300 or will display in an altered form for prices below $20.

<small>* humm reserves the right to change branding without prior notice</small>