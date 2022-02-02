---
title: "Code Samples: Using Magic-Summary in Javascript"
metaTitle: "Docs: Using Magic-Summary in Javascript with"
metaDescription: "Documentation on summarising text with the Magic-Summary AI model delivered via RapidAPI"
---

# Getting Started

Computational Magic, including Magic-Summary, use GraphQL - if you are not yet familiar with GraphQL, we highly recommend [HowToGraphQL](https://www.howtographql.com/).

The code samples below are supposed to provide a quick and easy way to get started with the Magic-Summary API in Computational Magic. Just copy the code, replace the placeholder with your own RapidAPI-key, pass in your strings you want to summarise (for example using templating with string literals in Javascript) and get going. 

# Isomorphic Fetch 

This is an exmaple of how to use `fetch` to call the Magic-Summary API. 

```javascript
fetch('https://magicsummary.p.rapidapi.com/api/v1', {
  method: 'POST',
  headers: { 'x-rapidapi-host': 'magicsummary.p.rapidapi.com', 'x-rapidapi-key': 'YOUR-RAPID-API-KEY-HERE', 'Content-Type': 'application/json' },
  body: JSON.stringify({ query: `
    query {
      summary(input: "YOUR LONG STRING HERE" )
        
      }
    }` 
  }),
})
.then(res => res.json())
.then(res => console.log(res.data));
```

# Using Axios

below is a code sample using Axios:

```javascript
var axios = require("axios").default;

var options = {
  method: 'POST',
  url: 'https://magicsummary.p.rapidapi.com/api/v1',
  headers: {
    'content-type': 'application/json',
    'x-rapidapi-host': 'magicsummary.p.rapidapi.com',
    'x-rapidapi-key': 'YOUR-RAPID-API-KEY-HERE'
  },
  data: {
    query: '{summary(input: "YOUR LONG STRING TO SUMMARISE HERE" )}'
  }
};

axios.request(options).then(function (response) {
	console.log(response.data);
}).catch(function (error) {
	console.error(error);
});
```