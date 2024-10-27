
###### 2024-10-25 15:08
###### Status:
###### Tags: [[System Design]]

# Combining of data systems

They all have different characteristics and there's different approach for each type of system too. 
Applications may have wide ranging requirements that a single tool cannot achieve those data processing and storage need alone. Instead the work get broken down into tasks that can be performed efficiently by a single tool, and get those different tools stitched together using __applciation code__.

#### Example
- application-managed caching layer (Memcahced or similar)
- full-text search server (Elasticsearch or Solr) separated from main database
![[IMG_7566.jpeg]]


# Reference
- [[Designing Data-Intensive Applications]] Chapter 1 p4