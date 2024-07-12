FROM python:3.12.4-slim-bullseye

RUN addgroup --gid 1000 jovyan && \
    adduser --system --shell /bin/false --ingroup jovyan --disabled-password --uid 1000 jovyan

RUN pip install varys-client climb-onyx-client plotly kaleido matplotlib pandas ipython

USER jovyan

CMD ["/bin/bash"]
