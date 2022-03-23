---
title: "Quickstart"
metaTitle: "Computational Magic: Documentation | Neuralfinity"
metaDescription: "Documentation for the AI API for the JAM stack age"
---


# Information about the BETA phase

**Please keep in mind that Computational Magic is in early BETA phase! If you plan to use it in production, we strongly advice to reach out to the team so we can ensure an uninterupted experience for you:**

[Contact Us](https://www.neuralfinity.com/#contact)

For more information on the beta phase, please see [Home](/)

# Quickstart Guide

If you already know how to work with GraphQL in your programming language, then here is what you need:

## Magic Summary

### Endpoint

Computational-Magic Platform: `https://beta.eu-north.computational-magic.com/api/v1`
Rapid-API: `https://magicsummary.p.rapidapi.com/api/v1`

### Authentication
For the Computational-Magic Platform you need to include headers for `x-api-key` with your API key as the value; 
For RapidAPI you need to add headers with `x-rapidapi-key` that includes your RapidAPI key as well as the `'x-rapidapi-host': 'magicsummary.p.rapidapi.com'` header. 

### Query:

The basic query syntax for Magic-Summary looks like this: 

```GraphQL
{summary(input: "your long string to be summarised")}
```
You have the following available arguments, but only `input` is required:

`input` *required*: a (longer) string to be summarised

`minLen: VALUE` *optional*: minium length of the return text (if not used, optimum default will be used)

`maxLen: VALUE` *optional*: maximum length of the return text (if not used, optimum default will be used)


