FROM amazoncorretto:21-al2023
RUN yum install -y procps-ng shadow-utils which wget

ENV NXF_HOME=/.nextflow

# copy docker client
RUN wget --directory-prefix /usr/local/bin/ https://github.com/nextflow-io/nextflow/releases/download/v24.04.4/nextflow

# download runtime
RUN mkdir /.nextflow \
    && chmod 755 /usr/local/bin/nextflow \
    && nextflow info

ENV PATH=/usr/local/bin:$PATH

RUN chown -R 1000:100 /.nextflow

USER 1000

CMD ["/bin/bash"]