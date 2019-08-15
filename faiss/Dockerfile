FROM conda/miniconda3

RUN conda update conda \
    && conda install -y mkl \
    && conda install -y faiss-cpu -c pytorch \
    && conda install -y flask \
    && conda install -y redis \
    && conda install -y uwsgi \
    && conda install -y flask_wtf \
