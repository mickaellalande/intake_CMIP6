# Intake CMIP6

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/mickaellalande/intake_CMIP6/main?urlpath=lab?filepath=CMIP6_global_projections.ipynb)

This repository is an experimental showcase for getting CMIP6 climate data with [Intake-esm](https://intake-esm.readthedocs.io/en/latest/).  The following packages are used:

- [Intake-esm](https://intake-esm.readthedocs.io/en/latest/): an intake plugin for parsing an Earth System Model (ESM) catalog and loading assets into xarray datasets.
- [xarray](http://xarray.pydata.org/en/stable/) is an open source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun! ([Xarray Tutorial](https://xarray-contrib.github.io/xarray-tutorial/) / [Xarray | SciPy 2020](https://www.youtube.com/watch?v=mecN-Ph_-78&list=PLYx7XA2nY5Gde-6QO98KUJ9iL_WW4rgYf&index=4))
- [ProPlot](https://proplot.readthedocs.io/en/latest/): a lightweight matplotlib wrapper for making beautiful, publication-quality graphics. 
(still in development)
- [xESMF](https://xesmf.readthedocs.io/en/latest/): Universal Regridder for Geospatial Data (only for Linux and Mac, an alternative is the [interp](http://xarray.pydata.org/en/stable/interpolation.html#example) function from xarray)
- [Dask](https://dask.org/) provides advanced parallelism for analytics ([jacobtomlinson/dask-video-tutorial-2020](https://github.com/jacobtomlinson/dask-video-tutorial-2020) / [Dask | SciPy 2020](https://www.youtube.com/watch?v=EybGGLbLipI&list=PLYx7XA2nY5Gde-6QO98KUJ9iL_WW4rgYf&index=6))

## Climate analysis

The purpose of this analysis will be to make a figure of the time series over the historical period, as well as projections for future scenarios.


## Where is this running?

This session is running on [binder.pangeo.io](https://binder.pangeo.io),
a service designed and maintained by the [Pangeo community](https://pangeo.io) for scalable earth science.
It is running on Google Cloud Platform using credits generously donated by Google to that Community.


## Other links
- See this great presentation: [Tech Talk: Intake](https://www.youtube.com/watch?v=urL17kRUinE&amp;feature=youtu.be) from [Aaron Spring](https://github.com/aaronspring/pydata_python_in_big_data_in_climate_science)
- [New climate simulation data models now available in Google Cloud](https://cloud.google.com/blog/products/data-analytics/new-climate-model-data-now-google-public-datasets)

## Manual installation

TODO



