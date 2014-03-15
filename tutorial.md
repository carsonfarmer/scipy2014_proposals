# Geospatial Data in Python: Database, Desktop, and the Web

## Brief Description

Using the wide range of tools and libraries available for working with geospatial data, it is now possible to transport geospatial data from a database to a web-interface in only a few lines of code. In this tutorial, we explore some of these libraries and work through examples which showcase the power of Python for geospatial data.

## Detailed Abstract

Tools and libraries for working with geospatial data in Python are currently undergoing rapid development and expansion. Libraries such as shapely, fiona, rasterio, geopandas, and others now provide Pythonic ways of reading, writing, editing, and manipulating geographic data. In this tutorial, participants will be exposed to a number of new and legacy geospatial libraries in Python, with a focus on simple and rapid interaction with geospatial data.

We will utilize Python to interact with geographic data from a database to a web interface, all the while showcasing how Python can be used to access data from online resources, query spatially enabled databases, perform coordinate transformations and geoprocessing functions, and export geospatial data to web-enabled formats for visualizing and sharing with others. We will also briefly explore Python plugin development for the QGIS Desktop GIS environment. Participants will go through the steps of creating a fully functional Python plugin for QGIS in an effort to demonstrate the rapid prototyping capabilities of Python and QGIS.

This tutorial should be accessible to anyone who has basic Python knowledge (though familiarity with Pandas, NumPy, matplotlib, etc. will be helpful) as well as familiarity with IPython Notebook. We will take some time at the start of the tutorial to go over installation strategies for geospatial libraries (GDAL/OGR, Proj.4, GEOS) and their Python bindings (Shapely, Fiona, GeoPandas) on Windows, Mac, and Linux. Some knowledge of geospatial concepts such as map projections and GIS data formats will also be helpful.

### Outline
- Introduction to geospatial data
    - Map projections, data formats, and looking at maps
- Introduction to geospatial libraries
    - GDAL/OGR (Fiona)
    - Shapely (GEOS)
    - PostGIS
    - GeoPandas
    - and more
- GeoPandas
    - Reading data from various sources
    - Data manipulation and plotting
    - Writing data to various sources
    - Getting data from the web
    - Pushing data to the web (for maps)
- Introduction to QGIS Desktop GIS
    - Python interface (PyQGIS)
    - Building a simple plugin
    - Plugin deployment

### Package List

pandas, numpy, scipy, fiona, shapely, geopandas, pyqgis, pyproj, descartes

### Additional Notes

Installing instructions from a previous year are [available here][install] and will be updated and made available to participants prior to the conference.

[install]: https://github.com/kjordahl/SciPy2013
