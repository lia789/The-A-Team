# **Data Business**


## **What are services we will offer?**
```
This is list of services we will offer on version 1:
1. Data Scraping (Avg price: 80$)
2. Leads Generation (Avg price: 50$)
3. Workflow Automation (Avg price: 100$)
4. Data Visualization (Avg price: 150$)
5. Data-Driven Desktop Applications (Avg price: 150$)
6. Data-Driven Web Applications (Avg price: 250$)
7. Web design (Avg price: 500$)

# Today Tomorrow we wil move on this list:
8. End to End Software Solutions (Avg price: 5,000-20,000$)
9. Machine Learning Algorithm (Avg price: 1500$)
10. Block Chain Algorithm (Avg price: 1500$)
```



## **How does we found client?**
```
Here is options for us rich out clients:
    1. Freelance Platform
    2. Real Estate (Website and Linkedin)
    3. E-commerce (Website and Linkedin)
```


## **Data Scraping**

```
Type of process about data scraping:
1. Simple Static Website
2. Simple Dynamic Website
3. Hidden API
4. Hard Dynamic Website

How does we analyze a website for data scraping?
1. Enable|Disable JavaScript
2. Wappalyzer Chrome Extension
3. Testing website on this site:
        - https://tools.pingdom.com/
        - https://gtmetrix.com/
4. Testing website on in house template code
5. Hidden API on Chrome Developer Tool



Data scraping project building steps:
1. Setup project structure
2. Write down design document
3. Create sample Google Sheet file
4. Write down Xpath code
5. Write down Python data scraping code
6. Run the code
7. Data clean and deliver the project
```


## **Xpath**
```
Xpath philosophy:
1. Xpath code should be solid.
2. The short code is good.
3. Xpath mistake cost huge and hard to found mistake
4. Two type of xpath code combination: 1. Single Element and 2 Loop Element
5. Same Xpath code will run lot of pages
```

```Python
# Xpath boiler code
from parsel import Selector

html_file_name = "h.html" # Change file name based on requirements
with open(html_file_name, "r") as f:
    html = f.read()
    response = Selector(text=html)

response
```

```
# Content selections code
//h1/text()
//a/@href()
//img/@src

# Element selection code
1. //tag
2. //tag [@attribute='value']
3. (//tag[@attribute='value'])[3]
4. //tag[contains(text(),'content')]                    # Text contain
5. //tag[contains(@attribute, 'value')]/text()          # Attribute
6. normalize-space()

```
```Python
# Example code single element
title = response.xpath("normalize-space(//h1[@id='title']/span/text())").get()
price = response.xpath("normalize-space(//span[@class='aok-offscreen']/text())").get()


# Loop elements
parent = response.xpath('//div[@class="products"]')

for product in parent:
    product_name = product.xpath('.//a/text()').get()
    product_url = product.xpath('.//a/@href').get()
```


## **Static Website**

```Python
# Request library example code
import requests

url = "https://quotes.toscrape.com/"

# Header
headers = {
    'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36'
    # more header can add here
}

# Query Parameters
query_parameters = {'search': 'laptop', 'page': 2} # Some request found query parameters

# Sending request
r = requests.get(url, params=params, headers=headers)
status_code = response.status_code
html = response.text




# API request code
url = "https://api.example.com/create"
payload = {
    'name': 'John Doe',
    'email': 'johndoe@example.com'
}

r = requests.post(url, json=payload, headers=headers)
response_json = r.json()
```


```Python
# Static website template code

import os
import csv
from parsel import Selector
from itertools import islice


# ======= Todo: Project settings =======
INPUT_CSV_FILE = "input.csv"
OUTPUT_CSV_FILE = 'output.csv'
SKIP_ROW = 0

URL_COUNTER = 1


# ==== Ignore setup code ====
def is_file_empty(file_path):
    """
    Check if the file is empty or does not exist.
    Returns True if the file does not exist or is empty.
    """
    return not os.path.exists(file_path) or os.stat(file_path).st_size == 0

file_empty = is_file_empty(OUTPUT_CSV_FILE)


# ==== Template code ======
with open(OUTPUT_CSV_FILE, 'a', newline='', encoding='utf-8') as file:
    writer = None

    with open(INPUT_CSV_FILE, 'r', encoding='utf-8') as f:
        reader = csv.DictReader(f)

        for row in islice(reader, SKIP_ROW, None):

            # ======= Todo: Use list of columns needed from input.csv file =======
            columns_name_1 = row['columns_name_1']
            columns_name_2 = row['columns_name_2']
            columns_name_3 = row['columns_name_3']

            # ======= Todo: Write down request code here =======
            # Example: Make an HTTP request to fetch HTML content
            # You can use requests or any other library
            # import requests
            # response = requests.get(row['url'])
            # html = response.text
            

            html = ""  # Replace with actual HTML fetching logic
            response = Selector(text=html)


            # ======= Todo: Write down Xpath code =======
            title = response.xpath("//h1/text()").get()
            price = response.xpath("//p/text()").get()



            # ======= Todo: Write down item_dic columns =======
            item_dic = {
                'columns_name_1': columns_name_1,
                'columns_name_2': columns_name_2,
                'columns_name_3': columns_name_3,
                'title': title,
                'price': price
            }


            # ==== Ignore csv file code ====
            if writer is None:
                field_names = item_dic.keys()  # Dynamic field names based on item_dic
                writer = csv.DictWriter(file, fieldnames=field_names)
                if file_empty:
                    writer.writeheader()
                    file_empty = False
            writer.writerow(item_dic)

            # ==== Ignore monitor code ====
            print(f"\rProcessing page number: {URL_COUNTER}...", end="")
            URL_COUNTER += 1

print("\nProcessing completed.")
```


## **Playwright**

```
Playwright command line tools:
$ pip install playwright
$ playwright install chromium
$ playwright codegen
```


```Python
# Playwright browser automation setup and testing code
from playwright.async_api import async_playwright

playwright = await async_playwright().start()
browser = await playwright.chromium.launch(
    headless=False,
    channel="chrome",
    # slow_mo=500,
    args=["--disable-blink-features", "--disable-blink-features=AutomationControlled"],
    # timeout=0
)
context = await browser.new_context(
    user_agent="Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36",
    # java_script_enabled=False
)
page = await context.new_page()  # This is the page object to reuse

url = "https://quotes.toscrape.com/js/"
await page.goto(url)
await page.wait_for_timeout(300)

# html for response
html = await page.content()

# Screen shoot of the page
await page.screenshot(path="screenshot.png")
```

```Python
# Simple dynamic website Playwright templates
import os
import csv
from parsel import Selector
from itertools import islice
from playwright.async_api import async_playwright

# ======= Todo: Project settings =======
INPUT_CSV_FILE = "input.csv"
OUTPUT_CSV_FILE = 'output.csv'
SKIP_ROW = 0

URL_COUNTER = 1


# ==== Ignore setup code ====
def is_file_empty(file_path):
    """
    Check if the file is empty or does not exist.
    Returns True if the file does not exist or is empty.
    """
    return not os.path.exists(file_path) or os.stat(file_path).st_size == 0
file_empty = is_file_empty(OUTPUT_CSV_FILE)


# ==== Playwright browser setup code ======
playwright = await async_playwright().start()
browser = await playwright.chromium.launch(
    headless=False,
    channel="chrome",
    # slow_mo=500,
    args=["--disable-blink-features", "--disable-blink-features=AutomationControlled"],
    # timeout=0
)

context = await browser.new_context(
    user_agent="Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36",
    # java_script_enabled=False
)

page = await context.new_page()


# ==== Template code ======
with open(OUTPUT_CSV_FILE, 'a', newline='', encoding='utf-8') as file:
    writer = None

    with open(INPUT_CSV_FILE, 'r', encoding='utf-8') as f:
        reader = csv.DictReader(f)

        for row in islice(reader, SKIP_ROW, None):



            # ======= Todo: Use list of columns needed from input.csv file =======
            columns_name_1 = row['columns_name_1']
            columns_name_2 = row['columns_name_2']
            columns_name_3 = row['columns_name_3']



            # ======= Todo: Write down Playwright code here =======
            # URL = ""
            # await page.goto(URL)
            # May need to click some button or website navigation code
            # await page.wait_for_timeout(300)

            
            # html for response
            html = await page.content()
            response = Selector(text=html)


            # ======= Todo: Write down Xpath code =======
            title = response.xpath("//h1/text()").get()
            price = response.xpath("//p/text()").get()




            # ======= Todo: Write down item_dic columns =======
            item_dic = {
                'columns_name_1': columns_name_1,
                'columns_name_2': columns_name_2,
                'columns_name_3': columns_name_3,
                'title': title,
                'price': price
            }



            # ==== Ignore csv file code ====
            if writer is None:
                field_names = item_dic.keys()  # Dynamic field names based on item_dic
                writer = csv.DictWriter(file, fieldnames=field_names)
                if file_empty:
                    writer.writeheader()
                    file_empty = False
            writer.writerow(item_dic)

            # ==== Ignore monitor code ====
            print(f"\rProcessing page number: {URL_COUNTER}...", end="")
            URL_COUNTER += 1




print("\nProcessing completed.")
```


## **Keyboard Shortcut**
```
# Ubuntu
1. Windows + C          # Chrome Open
2. Windows + T          # Terminal Open
3. Windows + E          # Text Editor
4. Alt + Tab            # Switch Application
5. Ctrl + Q             # Close Application (Except CMD|Terminal)
6. Windows + H          # Minimize Application.
7.Windows + Page Up     # Application Zoom In out
8. Windows + Page Down  # Application Zoom Out


# CMD
1. Ctrl + T                     # New Tab Open
2. ctrl + W                     # Closed Tab
3. Windows + H                  # Minimize 
4. Ctrl + Page Up|Page Down     # Change Tab
5. Ctrl+Shift+Q                 # Close Chrome browser


# VS-Code
1. code .                       # Open VS- code.
2. Ctrl + j                     # Terminal open|hide
3. Ctrl + Shift+E               # Activity bar file access
4. Ctrl + B                     # Activity bar open|hide
5. Ctrl + Page Up|Page Down     # Change work space tab
6. Shift+Enter                  # Run Python on Jupyter notebook
7. B                            # New cell on Jupyter notebook
8. D                            # Delete cell on Jupyter notebook
9. Ctrl + Z                     # Undo 
```



# **More topics will add soon**
```
Topics to add:
1. Some common browser action about Playwright
2. Playwright bypass bot protection feature code
3. Selenium setup code, template code and its details
4. Hidden API 
5. CSV file split and join code
6. Common data clean functions
7. Google Sheet integration setup code
8. More tools setup and integration setup code like Google sheet.
```








