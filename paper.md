# Pico data:
## Light-weight real-time event detection at the city level

Information pertaining to all facets of society, from public databases such as national census’, to private customer databases, to community-built open data sources, are increasingly being linked to geographical locations. Indeed, as much as 80% of all information held by business and government may be geographically referenced [2,9], and this number is only likely to grow as more organizations realize the importance of locational information [6].

Applications where real-time analysis of millions of temporally varying spatially referenced samples over wide geographical areas are required are becoming an everyday necessity. In addition to increasing volumes of sensor data produced by city infrastructures, real-time data feeds of users' activities through various applications such as Twitter [12], Flickr, Foursquare and others are becoming increasingly available. Location-aware applications and location-based services have become popular in recent years, such that many data feeds now have a geographic element by default. These 'digital footprints' provide a new means to understand 'the pulse of the city' -- how individuals, organizations, and communities utilize the places and spaces within their urban environment.

In this paper, the focus is on utilizing these types of information sources in order to automatically detect important events at the city level in real time. The goal is to provide city planners and businesses with information on '*what* is going on, and *when* and *where* it is happening'. Traditionally, this type of data analytics would require large investment in heavy-duty computing infrastructure, however, we suggest that in order to avoid the costs and limitations of data storage, management, and retrieval, a focus on real-time, focused analysis of data in a streaming framework is the most logical step forward: there is little sense in storing all the data if a model with a limited number of parameters is able to capture the phenomenon within a required level of accuracy.

Specifically, we utilize online Latent Semantic Analysis (LSA) techniques to extract 'topics' from Tweets in an online training fashion. This means the topic model is continually updated, and depending on parameterization, can 'forget' past topics in order to maintain real time relevance. We utilize the `gensim` Python package for LSA and other information retrieval (IR) functions. Based on a set of learned topics, we generate a grid of spatially located tweets for each identified topic, thereby highlighting areas where a particular topic occurs most frequently. The assumption here is that events may be directly tied to a particularly popular topic. Using an efficient streaming model for 2D kernel density estimation





Many cities are attempting to increase local prosperity and competitiveness by leveraging investments in ICT and related infrastructures. This so-called 'smart city' investment strategy depends on network-technology as a major source of growth. 

With this reliance on network-technologies comes an abundance of information on human interactions and mobility, including patterns of infrastructure, communications, and transportation usage. 
