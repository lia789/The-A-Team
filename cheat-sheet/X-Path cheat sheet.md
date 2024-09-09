# **X-Path**


## **X-Path Notebook Setup**
```
This is list of steps to follow setup Xpath notebook:
1. Project directory create
        $ mkdir project_name
2. Xpath notebook create
        $ touch project-name-xpath.ipynb
3. h.html file create
        $ touch h.html
4. Copy Python xpath boiler code
5. Copy html code from Chrome Browser
6. Run and check [response] 
```


## **XPath Boiler Code**

```python
from parsel import Selector

with open("h.html", "r") as f:
    html = f.read()
    response = Selector(text=html)


response
```



## **X-Path Two parts**
```
//h1/text()

1. Element selection   #  //h1/
2. Content Selection   #  /text()
```




## **Total X-Path Written 10 Rules**




## **X-Path Content Selection 3 Rules**
```
1. //tag/text()  # This on for text selection.
2. //tag@href    # This on for url selection
3. //tag@src     # This on for image selection
```

## **X-Path Element selection Two parts**

```
1. Support tag
2. End tag
``````


## **X-Path Element selection 6 Rules**

```
1. //tag
2. //tag [@attribute='value']
3. (//tag[@attribute='value']) [3]
4. //tag[contains(text()),'contain'] 
```