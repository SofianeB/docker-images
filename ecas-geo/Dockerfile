FROM jupyter/base-notebook
RUN conda config --set ssl_verify false
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

RUN conda install -vvv -c pyviz --yes \
          holoviews \
          geoviews \
          bokeh && \
    conda clean -tipsy
