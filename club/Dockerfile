FROM pytorch/pytorch:1.1.0-cuda10.0-cudnn7.5-runtime

RUN apt-get update && apt-get -y upgrade

RUN conda install -c anaconda libopencv opencv py-opencv

RUN conda install -c conda-forge \
RUN conda install -c \
                 matplotlib \
                 pydensecrf \
                 Pillow \
                 torch \
                 torchvision \
                 libiconv \
                 uwsgi \
                 flask \
                 cython \
                 tensorflow-gpu

RUN mkdir /tmp \
    && cd /tmp \
    && git clone https://github.com/thtrieu/darkflow.git \
    && cd darkflow \
    && python3 setup.py build_ext --inplace \
    && pip install -e .

CMD /bin/bash
