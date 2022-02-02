---
title: "Code Samples: Using Magic-Summary in Python"
metaTitle: "Docs: Using Magic-Summary in Python"
metaDescription: "Documentation on summarising text with the Magic-Summary AI model delivered via Computational Magic"
---

# Replace API key and content with your own

Please be sure to replace the placeholder API key with your API key and pass in your own strings for summarisation. 

# Using Requests

```python
import requests
 
url = "https://magicsummary.p.rapidapi.com/api/v1"

headers = {'x-rapidapi-host': 'magicsummary.p.rapidapi.com', 'x-rapidapi-key': 'YOUR-RAPID-API-KEY-HERE', 'Content-Type': 'application/json' }
 
query = """{summary(input: "INSERT YOUR LONG STRING HERE.")}"""

response = requests.post(url, headers=headers, json={'query': query})
print(response.status_code)
print(response.text)
```
