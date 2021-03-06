#Price-info Widgets on Shopify

1 - From the Shopify Dashboard, navigate to **Online Store > Themes > Actions > Edit Code**.

![theme-editor.png](/img/price-info/theme_edit.png)

2 - From left panel, navigate to **Sections** then select **product-template.liquid**.

> <b>If the "product-template.liquid" file does not exist</b>, navigate to **Templates** and select **product.liquid** instead.

3 - Place the below ```< script >``` tag in the desired place you'd like it to appear on your website. This should be added before the ```Add to Cart ``` button tag, or directly below the product price.

You will need to replace <code>PLACE_YOUR_MERCHANT_ID</code> with your unique merchant ID. This will have been provided to you in your welcome email.

```
<script src="https://bpi.humm-%country_abbr_lower_case%.com/%country_abbr_lower_case%/content/scripts/price-info_sync.js?productPrice={{product.selected_or_first_available_variant.price | divided_by: 100.00}}&merchantId=PLACE_YOUR_MERCHANT_ID"></script>
```

> **If you are unsure of your merchant ID, please reach out to pit@%domain%.**

4 - Save and you should see a working widget on your website.

<br>