
FROM jupyter/minimal-notebook

USER root

RUN apt-get update && apt-get install -yq --no-install-recommends \
    libjpeg-dev zlib1g-dev \
    && apt-get clean && \
    rm -rf /var/lib/apt/lists/*

ADD ./lab1/requirements.txt /root/
RUN pip install -r /root/requirements.txt


# Switch back to jovyan to avoid accidental container runs as root
USER jovyan
