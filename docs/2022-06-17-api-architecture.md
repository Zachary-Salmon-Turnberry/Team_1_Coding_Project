---
layout: post
title:  "api architecture"
parent: Overview
categories: jekyll architecture
nav_order: 1
---
## 1. API Architecture


## Status

Proposed

## Context

We need to develop REST API endpoints for web services being built by the web UI and mobile dev teams. This will allow them to access data needed by claim inspectors and field agents. Although both teams are using different systems, they both should be able to access information using the same method.  

<script src="https://unpkg.com/mermaid@9.1.2/dist/mermaid.min.js"></script>
<div class="mermaid">
flowchart TB

A([PDR Insurance])

B[Web App/Mobile App]



subgraph M[Turnberry Rest APIs]

direction LR

C[Apps make CRUD requests]-->D[REST APIs access database]

D-->F[APIs send information to front end apps]

end



subgraph N[Various Back Ends]

direction TB

H[Database]



end




B <--> M



M --HTTP Requests--> N

N --HTTP Responses--> M
</div>
## Decision

The API will be implemented with nodejs and express. This allows data to be accessed in a platform agnostic manner (using HTTP requests). 

## Consequences

The logic for creating responses will need to be done server-side. While this allows for multiple backends to be used, we will need to know what these are in advance to account for them.
