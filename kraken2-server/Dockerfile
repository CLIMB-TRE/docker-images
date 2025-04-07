FROM condaforge/mambaforge:latest AS conda

RUN /opt/conda/bin/mamba install -c conda-forge -c nanoporetech kraken2-server

CMD ["/bin/bash"]