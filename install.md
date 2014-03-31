# Installing Geospatial Python Libraries

These installation instructions are based largely on Kelsey Jordahl's [2013 SciPy tutorial][]: [Using Geospatial Data With Python][].

## Required packages

- [PyProj][] Python interface to PROJ.4 library
- [Shapely][] Pythonic library for geometric tasks
- [Fiona][] Pythonic interface to OGR data formats
- [GeoPandas][] Support for geographic data in pandas objects
- [pySpatiaLite][] Python interface to lightweight spatial database

## Optional packages

- [Basemap][] Plot on map projections using matplotlib
- [gdal][] Python bindings for Geospatial Data Abstraction Library (and OGR)
- [Cartopy][] Advanced mapping interface for python
- [Descartes][] Create matplotlib Patch objects from Shapely geometries
- [geoJSON][] reference implementation of the Python geo interface
- [psycopg2][] for connection to PostgreSQL/PostGIS database
- [SQLAlchemy][] Object Relational Model for SQL databases

[PyProj]: http://code.google.com/p/pyproj
[Basemap]: https://github.com/matplotlib/basemap
[Cartopy]: http://scitools.org.uk/cartopy
[Descartes]: https://pypi.python.org/pypi/descartes
[geoJSON]: https://pypi.python.org/pypi/geojson
[gdal]: https://pypi.python.org/pypi/GDAL
[Shapely]: http://toblerity.github.io/shapely
[Fiona]: http://toblerity.github.io/fiona
[psycopg2]: https://pypi.python.org/pypi/psycopg2
[SQLAlchemy]: http://www.sqlalchemy.org
[GeoPandas]: https://github.com/kjordahl/geopandas
[pySpatiaLite]: https://github.com/lokkju/pyspatialite
[2013 SciPy tutorial]: https://github.com/kjordahl/SciPy2013
[Using Geospatial Data With Python]: http://kjordahl.github.io/SciPy2013

## Installation instructions

The standard [scientific python stack][] is a prerequisite for this tutorial before installing the specific packages listed above.  I recommend starting with a standard scientific python distribution such as [Enthought Canopy][] or [anaconda][]. Other package managers such as Linux distribution tools or [homebrew][] for OS X will work for a starting point as well, though I have not tested these. On Windows you may be able to use [Christoph Golke's binary packages][].

Install the above packages via your standard package manager when possible.  For packages not available in this way (or if you wish to use a different version than available), you may install directly with `pip` or `easy_install`.  For example, to install Shapely, you may use::

    pip install shapely

Finally, if all else fails, or you wish to be on the bleeding edge, you may install packages from source.  For example::

    git clone https://github.com/Toblerity/Shapely
    cd Shapely
    python setup.py install

will install the current development version of Shapely.

Serge Ray has shared [his setup notes][] from last year for OS X 10.8.4 and anaconda. 

[Enthought Canopy]: https://www.enthought.com/products/canopy
[anaconda]: https://store.continuum.io/cshop/anaconda
[scientific python stack]: http://www.scipy.org/install.html
[Christoph Golke's binary packages]: http://www.lfd.uci.edu/~gohlke/pythonlibs
[his setup notes]: https://github.com/kjordahl/SciPy2013/blob/master/osx-anaconda.md
[homebrew]: http://brew.sh/

### Known installation issues

- GDAL binary libraries may not be found even when they are installed, particularly when installing fiona.  The fiona install process uses the command `gdal-config --cflags` to find header files.  This should match your GDAL install location.
- You may need to install GDAL on your system.  A number of [binaries][] are available, or you could use a package manager such as `fink` or `apt-get`, or build it from source.
- You will also probably have to install SpatiaLite on your system. You can get binaries [from here][]. Once that is installed, getting pySpatiaLite is as simple as `pip install pyspatialite`.

[binaries]: http://trac.osgeo.org/gdal/wiki/DownloadingGdalBinaries
[from here]: http://www.gaia-gis.it/spatialite-2.4.0-4/binaries.html
