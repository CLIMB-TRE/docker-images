FROM python:3.12-alpine

RUN addgroup --gid 1000 jovyan && \
    adduser --system --shell /bin/false --ingroup jovyan --disabled-password --uid 1000 jovyan

RUN pip3 install varys-client climb-onyx-client plotly kaleido=0.2.1 matplotlib pandas ipython

USER jovyan

CMD ["/bin/bash"]
