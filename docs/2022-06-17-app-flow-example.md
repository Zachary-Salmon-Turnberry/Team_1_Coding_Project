---
layout: post
title:  "app flow example"
categories: jekyll example
parent: Overview
nav_order: 1
---
## 2. Example


## Status

Proposed

## Context

Inspector Clouseau the Claim Inspector is out in the field assessing a car crash involving Mr. Bond, who has PDR Insurance. Clouseau pulls out his iPhone and opens up the handy dandy PDR Insurance mobile application to search for Mr. Bond's informaiton. Behind the scenes, the application is performing an HTTPS GET request using one of the API endpoints developed by Turnberry Solutions. This endpoint processes the HTTPS request and sends Mr. Bond's information from the database to the front end to be displayed. Clouseau then adds a new claim to Mr. Bond's profile and fills in the relevant information for this claim. Clouseau then gets Mr. Bond's signature consenting to store this information in the PDR Insurance database and presses the save button which performs an HTTPS PUT request to add the new information to Adam’s table in the database. 

<script src="https://unpkg.com/mermaid@9.1.2/dist/mermaid.min.js"></script>
<div class="mermaid">
flowchart TB
    A([Mr. Bond crashes car]) --> B[Inspector Clouseau arrives]
    
    subgraph M[POLICY LOOKUP]
        direction LR
        C[IC Opens iOS app and enters info]-->D[App sends HTTP GET request]
        D-->F[Server fetches Mr. Bond's info from backend]
        F-->G[App loads policy]
    end

    subgraph N[ADD CLAIM]
        direction LR
        H[IC enters claim info] --> I[IC passes device to Mr. Bond for consent signature]
        -->J[App sends HTTP POST request] 
        J --> K[Server processes request]
        K-->L[Encrypted claim information is created in database]
    end



    B--> M --> N
</div>