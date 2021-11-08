FROM robertobucher/pysimcoder:latest

RUN apt-get -y update
RUN apt-get -y dist-upgrade

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
    
COPY . /app
CMD ["/app/entrypoint.sh"]
EXPOSE 8080

