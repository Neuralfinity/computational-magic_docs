---
title: "Code Samples: Using Magic-Summary in Javascript"
metaTitle: "Docs: Using Magic-Summary in Javascript"
metaDescription: "Documentation on summarising text with the Magic-Summary AI model delivered via Computational Magic"
---

# Getting Started

Computational Magic, including Magic-Summary, use GraphQL - if you are not yet familiar with GraphQL, we highly recommend [HowToGraphQL](https://www.howtographql.com/).

## Using Apollo



```javascript
import { useQuery, gql } from '@apollo/client';

const FEED_QUERY = gql`
  {summary(input: "your long string to be summarised")}`;

```

## Using Isomorphic Fetch 

```javascript
require('isomorphic-fetch');

fetch('https://beta.eu-north.computational-magic.com/api/v1', {
  method: 'POST',
  headers: { 'x-api-key': 'YOUR API KEY HERE', 'Content-Type': 'application/json' },
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