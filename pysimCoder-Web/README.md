# pysimCoder in a WEB browser

This dockerfile has been generated starting from the files available at https://github.com/theasp/docker-novnc.

Many thanks to Andrew Phillips for the provided image!

In the Dockerfile it is possible to the following variables:

* `DISPLAY_WIDTH=<width>` (1024)
* `DISPLAY_HEIGHT=<height>` (768)

Launch the docker image using
```
$ docker run --rm -it -p 8080:8080 --privileged robertobucher/pysimcoder:novnc
```
Open a browser and go to  `http://<server>:8080/vnc.html`

In the terminal launch
```
psc
```


