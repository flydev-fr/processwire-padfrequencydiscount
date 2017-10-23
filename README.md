# PadLoper Frequency Discount

ProcessWire module that adds the possibility to add frequency discounts by product category.

If you've never heard of PadLoper - it’s an easy and flexible eCommerce platform, built on the ProcessWire framework. [Find out more about Padloper](https://padloper.pw/) or [just go for it](https://padloper.pw/buy/).


## Howto

1. Download and install the module
2. Add template for frequency discount pages (*shop-item-discount* for example) and add the following fields (name them as you like): 
    - **title** – will be shown as product title
    - **pad_price** *(float)* – must be the same field which is  set in module settings from PadCart as pricefield; later you have to enter a negative value, all products with this category will get this discount per product
    - **quantity** *(Integer)* – minimum amount of products needed for the discount
    - **category** *(Options)* – must be the same field as used as category in the product template(s), it holds the category for which the discount counts
3. Edit the previously installed module, assign templates and fields
    - templates for checkout and frequency discount
    - fields used as category and quantity
4. Edit **PadCart** module, add frequency discount template as product template
5. Add pages for each frequency discount per product category

Well, that's all.  
Add some products with a specific category to the cart, if the number exceeds the configured quantity, the checkout product table gets one more row containing the frequency discount.

## Example

> If the customer purchases at least **three** products with the category **product**, he’ll get a frequency discount of **3EUR** per product.

Add a new page, assign the previously created frequency discount template and add the following values:

| title              | price | quantity | category |
|--------------------|-------|----------|----------|
| Frequency Discount | -3    | 3        | product  |

![Checkout Product Table](https://github.com/justb3a/processwire-padfrequencydiscount/blob/master/checkout-table.jpg)
