# Light-weight real-time event detection with Python

## Brief Description

Real-time feeds of user activity from various apps such as Twitter, Foursquare, and others are becoming increasingly available. These 'digital footprints' provide new means to understand how individuals utilize the places and spaces of urban environments. We present a light-weight framework for real-time event detection in a city based on existing SciPy libraries and real-time Twitter streams.

## Detailed Abstract

In this paper, we utilize real-time 'social information sources' to automatically detect important events at the urban scale. The goal is to provide city planners and others with information on *what* is going on, and *when* and *where* it is happening. Traditionally, this type of analysis would require a large investment in heavy-duty computing infrastructure, however, we suggest that a focus on real-time analytics in a lightweight streaming framework is the most logical step forward.

Using online Latent Semantic Analysis (LSA) from the [`gensim`][gensim] Python package, we extract 'topics' from tweets in an online training fashion. To maintain real-time relevance, the topic model is continually updated, and depending on parameterization, can 'forget' past topics. Based on a set of learned topics, a grid of spatially located tweets for each identified topic is generated using standard `numpy` and `scipy.spatial` functionality. Using an efficient streaming algorithm for approximating 2D kernel density estimation (KDE), locations with the highest density of tweets on a particular topic are located. Locations are semantically labeled using the learned topics, based on the assumption that events can be directly tied to a particularly popular topic at a particular location.

To facilitate real time visualization of results, we utilize the [`pico`][pico] Python/Javascript library as a real-time bridge between server-side Python analysis and client-side Javascript visualization. This enables fast, responsive interactivity of computationally intensive tasks. Additionally, since `pico` allows streaming data from Python to Javascript, updates to the web-interface are sent and consumed as needed, such that only significant changes in an event's status, or the introduction of a new event, will cause updates to the visualizations. Finally, because all models, data structures, and outputs on the server side are pickle-able Python objects, this entire framework is small enough to be deployed on almost any server with Python installed.

[pico]: https://github.com/fergalwalsh/pico
[gensim]: https://github.com/piskvorky/gensim/
