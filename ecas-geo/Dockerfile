FROM jupyter/base-notebook
ARG JUPYTERHUB_VERSION=0.9.4
RUN conda config --add channels conda-forge
RUN conda config --add channels pyviz
RUN conda install -c conda-forge --quiet --yes \
          xarray \
          dask \
          distributed \
          graphviz \
          netCDF4 \
          bottleneck \
          basemap \
          ipywidgets \
          'tornado < 6' \
          cartopy && \
   conda clean -tipsy

RUN conda install -c pyviz --yes \
          holoviews \
          geoviews \
          bokeh && \
    conda clean -tipsy
