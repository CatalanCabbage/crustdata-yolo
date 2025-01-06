# crustdata-yolo
The [Crustdata build challenge](https://docs.google.com/document/d/1xO8sFtVMyOMtElGCd0vZtzXQAGVFNFo9a9Xkfxu2yQA/preview?tab=t.0#heading=h.h39yx7l547to)

## Requirements
Data: 
- [All APIs, Discovery & enrichment](https://crustdata.notion.site/Crustdata-Discovery-And-Enrichment-API-c66d5236e8ea40df8af114f6d447ab48#f531a93b8e2d4bb1899ba6067c12c2d7) - get company data, filter companies, get LinkedIn posts etc
- [Dataset API details](https://crustdata.notion.site/Crustdata-Dataset-API-Detailed-Examples-b83bd0f1ec09452bb0c2cac811bba88c#ff964b2e316c49de8770e0bf2cf81f8a) - get specific data like reviews, web traffic, investors etc
- [Data dictionary](https://crustdata.notion.site/Crustdata-Data-Dictionary-c265aa415fda41cb871090cbf7275922) - definitions for all fields used in the APIs etc

Goals:  
- **Basic static chat**: Ask questions about APIs in a chat interface
- **Dynamic validation**: Validate API call answers, fix using error logs from response
- **Ingestion of additional knowledge base**: Add QnAs, update documentation and APIs
- **Slack integration**  Works on specific channels and users, drafts a response

## Drafts
Plan: 
1. Extract docs data into a custom DB
2. Have a RAG step that fetches the API most suitable to the user's query from our custom DB
3. Share this as context to the LLM to answer the query. If API is involved, get API code back for validation.
4. For API additions/mods: update custom DB
5. For QnAs: add as additional context (either in the 1st LLM call or after that if )

Questions:
|???|Reason?|Answer|
|----|----|----|
|What kind of APIs are present, how are they distinct?|Will decide how sophisticated RAG needs to be||
|What context is needed by LLM to draft one API?|Will decide what data needs to be extracted in RAG||


Cases: Maybe the question has nothing to do with APIs
