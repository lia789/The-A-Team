# **Xpath**


## **Xpath Philosophy**
```
Here is the list of Xpath philosophy:
1. We learn Xpath for extracting content form website.
2. Xpath use for selecting elements and web automation process like click button, fillup box, etc.
3. Xpath code should as solid as possible, same code will use lot of web pages
4. Xpath code as short as good, that have less probability to break in future
5. Xpath mistake cost huge and hard to found mistakes on large dataset
6. XPath code combination of supported tags, end tags and content tags
7. ChatGPT help us write bext xpath code
8. Two type of Xpath code combinations are there: 1. Single Element  2. Using For Loop
```


## **XPath Boiler Code**

```python
from parsel import Selector


html_file_name = "h.html" # Change file name based on requirements
with open(html_file_name, "r") as f:
    html = f.read()
    response = Selector(text=html)

response
```

## **Xpath Code Snipe**
```
Content selections code:
//h1/text()                       -> Text content extraction
//a/@href()                       -> Url content extraction
//img/@src                        -> Image content extraction
```

```
Single elements code:
1. //tag                                                  -> Selecting with tag
2. //tag [@attribute='value']                             -> Selecting attribute and value
3. (//tag[@attribute='value'])[3]                         -> Selecting by index
4. //tag[contains(text(),'contant')]                      -> Partial content match
5. //tag[contains(@attribute, 'value')]/text()            -> Partial value match
```

## **For loop**
```python

import parsel

# Example HTML content
html_content = """
<div class="products">
  <div class="product">
    <a href="https://example.com/product1">Product 1</a>
  </div>
  <div class="product">
    <a href="https://example.com/product2">Product 2</a>
  </div>
  <div class="product">
    <a href="https://example.com/product3">Product 3</a>
  </div>
</div>
"""

# Create a selector object using parsel
selector = parsel.Selector(html_content)

# Select the parent 'products' div
parent = selector.xpath('//div[@class="products"]')

# Loop through each child 'product' div and extract the product details
for product in parent.xpath('.//div[@class="product"]'):
    # Extract product name and URL
    product_name = product.xpath('.//a/text()').get()
    product_url = product.xpath('.//a/@href').get()
    
    # Print the extracted data
    print(f"Product Name: {product_name}")
    print(f"Product URL: {product_url}")
    print('---')
```
