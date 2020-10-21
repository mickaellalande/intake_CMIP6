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



---

## Manual installation (tested only on Linux)
If you want to run this code on your own computer, follow the next steps: 

1. **Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html)** (for Linux):
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
sh Miniconda3-latest-Linux-x86_64.sh 
```
You should have a `(base)` in front of your line in your terminal, that correspond to the **root** environment.

2.  **Add [conda-forge](https://conda-forge.org/docs/user/introduction.html)** and **update** your installation:  
```bash
conda config --add channels conda-forge  
conda config --set channel_priority strict  
conda update -n base -c defaults conda  
```
3. **Create an environment** (it is recommended not to use the root environment so that you keep a clean installation: [https://conda-forge.org/docs/user/introduction.html](https://conda-forge.org/docs/user/introduction.html)):
```bash
conda create -n intake_CMIP6_v0
```
```bash
conda activate intake_CMIP6_v0
```
```bash
conda install xarray netcdf4 nc-time-axis xesmf esmpy \
dask python-graphviz dask-labextension "nodejs>=10.0" nbresuse \
intake-esm gcsfs zarr "proplot=0.6.4" "matplotlib=3.2.0" cartopy \
jupyter jupyterlab nb_conda_kernels
```
```bash
# For testing xESMF (for regrid)
pip install pytest  
pytest -v --pyargs xesmf #all need to pass
```
```bash
# Install dask-labextension
jupyter labextension install dask-labextension
jupyter serverextension enable dask_labextension
```
```bash
jupyter lab
```

Alternatively you can install directly from the environment file instead of step 3:
```bash
conda env create -f envs/intake_CMIP6_v0.yml
```

More information about environments: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html








