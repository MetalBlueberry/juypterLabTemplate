FROM jupyter/minimal-notebook:ad3574d3c5c7

USER root 
## RUN apt-get if you need it

USER jovyan

COPY requirements.txt .
RUN pip install -r requirements.txt

ENV JUPYTER_ENABLE_LAB=yes

RUN jupyter labextension install jupyterlab_vim && \
    jupyter labextension install @jupyterlab/dataregistry-extension && \
    pip install --upgrade jupyterlab-git && \
    jupyter lab build
