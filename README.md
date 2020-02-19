![POLITICO](https://rawgithub.com/The-Politico/src/master/images/logo/badge.png)

# nicar-2020-geopandas

This repo contains the files for the #NICAR20 session "[Mapping in Python](https://ireapps.github.io/nicar-2020-schedule#20200308_mapping_in_python_2486)".

From the session description:

> Learn how to use GeoPandas, a handy Python library that lets you do powerful geospatial analysis from the comfort of a Jupyter Notebook. We'll cover mapping, filtering and merging datasets, changing between projections and formatting publication-ready maps.

## Intro

[GeoPandas](https://geopandas.org/) is a powerful Python library that extends [pandas](https://pandas.pydata.org/) with geospatial analysis tools.

It's a great alternative to QGIS or standalone PostGIS queries because — like pandas or R — it enables scripted, repeatable and shareable analysis.

We'll be using GeoPandas within a [Jupyter Notebook](https://jupyter.org/), an excellent tool for writing, annotating and storing Python code used in analyses.

A smart note from Scott Pham, who led [a similar session](https://www.ire.org/events-and-training/event/3190/4248) at NICAR 2019:

> It's important to realize that GeoPandas is really just a nice wrapper around a bunch of other useful Python libraries including Pandas, Matplotlib, Fiona, Shapely and others. If you want to do something complicated that's not covered by the GeoPandas documentation, there's a good chance you can still do it by looking at the documentation for one of those other libraries.


## What's in here

- **[`./notebooks/`](notebooks/)**: The four notebooks we'll be using throughout this session.
- **[`./source_data/`](source_data/)**: The data files these notebooks load for analysis and mapping.
- **[`./output-images/`](output-images/)**: An empty folder where the notebooks will export images of finished maps.
- **[`./Pipfile`](Pipfile)**: A list of dependencies needed to run this tutorial.


## Related reading

- [Geopandas reference](http://geopandas.org/install.html)
- [Jonathan Soma's excellent geopandas tutorials](http://jonathansoma.com/lede/foundations-2017/classes/geopandas/mapping-with-geopandas/)
- [Reference for getting CRS/EPSG numbers](https://epsg.io/4326)
- [Pyplot options](https://matplotlib.org/3.0.2/api/_as_gen/matplotlib.pyplot.plot.html#matplotlib.pyplot.plot)
- [Spatial join example](https://github.com/datadesk/geopandas-spatial-join-example)
- [Matplotlib colormaps](https://matplotlib.org/users/colormaps.html)
- [Matplotlib named colors](https://i.stack.imgur.com/lFZum.png)
- [Scott Pham's NICAR 2019 course materials](https://github.com/scottpham/nicar19-geopandas)


## Requirements

- Pipenv ([installation instructions](https://pipenv.readthedocs.io/en/latest/install/))
- Python 3.6
- GeoPandas dependencies (including GDAL, GEOS and PROJ; [installation guide here](https://geopandas.org/install.html#dependencies))


## Installation

1. Clone this repo and `cd` into it:

    ```sh
    $ git clone git@github.com:The-Politico/nicar-2020-geopandas.git
    $ cd nicar-2020-geopandas
    ```

2. Set up a Python 3.6 virtual environment, step into it and install dependencies:

   ```sh
    $ pipenv shell
    $ pipenv install --dev
    ```

## Usage

To launch the Jupyter Notebook service, run the following command in this folder:

```sh
$ pipenv run jupyter notebook
```

A Jupyter Notebook process should launch and open a tab in your web browser. From there you should be able to navigate to the `notebooks/` folder and begin navigating through the four notebook files (each of which is described below).

#### Notebooks used in this tutorial

_All notebooks can be found in the `./notebooks/` directory._

-   `01__simple-mapping.ipynb`

    **What it covers**: Importing polygon shapefiles, map styling, generating simple choropleth maps.

-   `02__meaningful-choropleth.ipynb`

    **What it covers**: Filtering polygon shapefile to a subset of features, creating derived fields, merging data files on a unique identifier.

-   `03__points-atop-polygons.ipynb`

    **What it covers**: Importing and filtering point shapefiles, mapping points and polygons simultaneously.

-   `04__geospatial-merge.ipynb`

    **What it covers**: Changing coordinate systems of data, merging point data with that of containing polygons, grouping and counting how many points are in a given polygon.
