# Start from a core stack version
FROM jupyter/scipy-notebook
# Install in the default python3 environment
USER root
RUN apt-get -y update
RUN apt-get install -y zlib1g-dev \
	liblcms2-dev \
	libwebp-dev  \
	libgeos-dev
USER jovyan
RUN conda install -c conda-forge proj4=5.2.0
# Install the Python Requirements
ADD requirements.txt /tmp/
RUN cd /tmp && \
    pip install -r requirements.txt 
