
###### 2024-11-02 21:15
###### Status: 
###### Tags: [[System Design]] [[CS Theory]]

# Web Scraping Challenges

#### Challenges
- Graph being directed
	- we can view web scraping as graphs, pages being the vertex and hyperlink being the edge. Links are usually one-sided (page a references b, but not otheriwise), thus graph must be directed
	1. not all vertices in graph are [[strongly connected component]] (in graph 5.1, can reach 5 from 1 but not otherwise)
	2. Traversing directed graph needed different algorithm than normal graphs
- cannot count all vertices
	- When traversing graphs, we need to know all the vertex when checking if a traversal is complete (without any unvisited vertex), which is not achievable in web scraping
- vertex and edge being dynamic
	- say we retrieved a list of all hyperlinks and would visit them one by one, by the time we visit one page, it may not exists any more, or the hyperlink in its parent was updated to a new page/newer version of the page, we would lose them
- Volume/Scale issue
	- Latency from the handshake always exists even in the fastest network, and we might also need to go through multiple servers to retrieve a page.
- coordination problems in Parallelism
	- making sure multiple servers are not doing repeated tasks
		- could send a message from server A when finishing the task to other servers, but this is limited by bandwidth when there's too many servers to notify
	- **solution**: [[Distributed Systems]]
		- distributed decisions and centralised coordination
		- having 1 lead server for coordination
		- individual server doesn't need lead's permission to know what page to download. if not its own task to download a certain page, notify lead
		- distributing task approach: IP address, could be disproportional so relies on experience of engineers. (PHQ approach, unique id and distributed to [[Kafka Partitions]] with murmur2_random (hash))
- rate limit


# Related pages
- ![[Screen Shot 2024-11-02 at 9.20.53 PM.png]]

# Reference
- [[计算之魂]]