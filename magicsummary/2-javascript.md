---
title: "Using Magic-Summary in Javascript"
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