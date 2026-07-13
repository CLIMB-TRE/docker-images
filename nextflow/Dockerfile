FROM amazoncorretto:21-al2023
RUN yum install -y procps-ng shadow-utils which wget

ENV NXF_HOME=/.nextflow

# copy docker client
RUN wget --directory-prefix /usr/local/bin/ https://github.com/nextflow-io/nextflow/releases/download/v26.04.6/nextflow

RUN mkdir /.nextflow \
    && chmod 755 /usr/local/bin/nextflow \
    && nextflow info

ENV PATH=/usr/local/bin:$PATH

ENV NXF_SYNTAX_PARSER=v1

RUN chown -R 1000:100 /.nextflow

USER 1000:100

CMD ["/bin/bash"]
