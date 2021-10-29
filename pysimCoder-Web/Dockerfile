FROM debian:11-slim

RUN apt-get -y update
RUN apt-get -y dist-upgrade

RUN apt-get -y install \
    gcc \
    gfortran \
    git \
    cmake \
    binutils \
    emacs \
    python3.9 \
    python3-numpy \
    python3-scipy \
    python3-sympy \
    python3-matplotlib \
    python3-pip \
    jupyter-qtconsole \
    python3-lxml \
    python3-pyqtgraph \
    libopenblas-dev \
    liblapack-dev \
    libxml2-dev \
    libcomedi-dev \
    python3-pyqt5

RUN set -ex; \
    apt-get install -y --no-install-recommends\
      blackbox \
      net-tools \
      novnc \
      supervisor \
      x11vnc \
      xfce4-terminal \
      xvfb
  
RUN apt-get -y clean
RUN apt-get -y autoremove

# Setup demo environment variables
ENV HOME=/root \
    DEBIAN_FRONTEND=noninteractive \
    DISPLAY=:0.0 \
    DISPLAY_WIDTH=1600 \
    DISPLAY_HEIGHT=1024 \
    RUN_XTERM=yes \
    RUN_FLUXBOX=yes
    
WORKDIR .
RUN git clone https://github.com/robertobucher/pysimCoder

WORKDIR ./pysimCoder
RUN make -f make4docker.mak

COPY . /app
CMD ["/app/entrypoint.sh"]
EXPOSE 8080

