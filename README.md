# AI-App-Capstone

## Overview

For our Senior Capstone project, I worked as a developer alongside four other team members to create an AI troubleshooting assistant named Pin. Using Retrieval-Augmented Generation (RAG), the assistant solves employees' Tier 0 and Tier 1 IT issues using company-specific troubleshooting methodologies. By using software like Pin, an organization can drastically reduce repetitive lower-tier tickets from taking up valuable help desk time. 

## Video Demo

[Watch it here.](https://www.youtube.com/watch?v=oRqLPXB6qPk)

## Features

- Easy-to-use chat interface  
- 100 document knowledge base  
- Retrieval-Augmented Generation (RAG)  
- Ticket creation  
- Safety guardrails  

## Tech Stack

- Python  
- FastAPI  
- Large Language Models (Gemini models used for demos)  
- Retrieval-Augmented Generation (RAG)  
- SQLite  

## AI Architecture

1. The process begins when a user asks a question in the system.

2. The system converts the user’s query into a vector embedding.

3. The embedding is used to search the knowledge base for the most relevant content.

4. Retrieved knowledge base entries are added to the prompt as contextual information.
   
5. The prompt (user query + relevant context) is sent to the language model.

6. The LLM generates a response grounded in company troubleshooting policies and documentation.

## Guardrails

Our system thinks beyond troubleshooting issues. We have custom guardrail logic that checks each LLM response for banned phrases such as "disable antivirus". Once detected, the system blocks the response and asks the user to try again with another question. This protects the organization from unsafe/noncompliant IT advice.
