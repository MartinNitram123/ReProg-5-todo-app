FROM python:3.10-slim

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends apt-utils 2>&1 \
    && apt-get install -y git procps lsb-release pandoc texlive-xetex

RUN pip install jupyter jupyterlab

RUN apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

USER vscode
