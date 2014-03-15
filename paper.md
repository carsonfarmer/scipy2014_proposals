# Light-weight real-time event detection at the city level

Applications where real-time analysis of millions of temporally varying spatially referenced samples over wide geographical areas are required are becoming an everyday necessity. In addition to increasing volumes of sensor data produced by city infrastructures, real-time data feeds of users' activities through various applications such as Twitter, Flickr, Foursquare and others are becoming increasingly available. Location-aware applications and location-based services have become popular in recent years, such that many data feeds now have a geographic element by default. These 'digital footprints' provide a new means to understand 'the pulse of the city' - how individuals, organizations, and communities utilize the places and spaces within their urban environment.

In this paper, the focus is on utilizing these types of information sources in order to automatically detect important events at the city level in real time. The goal is to provide city planners and businesses with information on '*what* is going on, and *when* and *where* it is happening'. Traditionally, this type of data analytics would require large investment in heavy-duty computing infrastructure, however, we suggest that in order to avoid the costs and limitations of data storage, management, and retrieval, a focus on real-time, focused analysis of data in a lightweight streaming framework is the most logical step forward.

Specifically, we utilize online Latent Semantic Analysis (LSA) techniques to extract 'topics' from tweets in an online training fashion. This means the topic model is continually updated, and depending on parameterization, can 'forget' past topics in order to maintain real time relevance. We utilize the `gensim` Python package for LSA and other information retrieval (IR) functions. Based on a set of learned topics, we generate a grid of spatially located tweets for each identified topic, thereby highlighting areas where a particular topic occurs most frequently. This is done using `numpy` and `rtree` Python packages. The assumption here is that events may be directly tied to a particularly popular topic. Using an efficient streaming algorithm for approximating 2D kernel density estimation, we identify locations with the highest density of tweets on a particular topic, and semantically label that location with the learned topic. This is done using `scipy` and friends. 

In order to facilitate 


Extensions to this relatively simple framework include explicit extraction of location information from the tweets themselves, as well as multi-scale topic density grids.

we take advantage of pico to ease web-interactivity and the ability to 'stream' updates to the browser?

real-time bridge between server side python analysis and javascript visualisation
