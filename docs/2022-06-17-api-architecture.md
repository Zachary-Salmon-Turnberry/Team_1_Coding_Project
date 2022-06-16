---
layout: post
title:  "api architecture"
categories: jekyll architecture
---
## 1. API Architecture


## Status

Proposed

## Context

We need to develop REST API endpoints for web services being built by the web UI and mobile dev teams. This will allow them to access data needed by claim inspectors and field agents. Although both teams are using different systems, they both should be able to access information using the same method.  

## Decision

The API will be implemented with nodejs and express. This allows data to be accessed in a platform agnostic manner (using HTTP requests). 

## Consequences

The logic for creating responses will need to be done server-side. While this allows for multiple backends to be used, we will need to know what these are in advance to account for them.
