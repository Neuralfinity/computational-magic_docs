---
title: "Code Samples: Using Magic-Summary in Python"
metaTitle: "Docs: Using Magic-Summary in Python"
metaDescription: "Documentation on summarising text with the Magic-Summary AI model delivered via Computational Magic"
---


# Using Requests

```python3
import requests
 
url = "https://beta.eu-north.computational-magic.com/api/v1"

headers = {'x-api-key': 'INSERT YOUR API KEY HERE!'}
 
query = """{summary(input: "INSERT YOUR LONG STRING HERE.")}"""

response = requests.post(url, headers=headers, json={'query': query})
print(response.status_code)
print(response.text)
```


you can use fstrings to make it easier to pass an object into your query. 
That would look like this: 

```python3

```