# pysimCoder_Docker

The two folders contain two versions of Dockerfile for generating two different images of pysimCoder.

The pysimCoder_X folder contains a Dockerfile that can generate an image that should be run using X support.

The pysimCoder_Web folder contains a Dockerfile which generate an image that can be run from a browser.

It is possible to get both images directly from the Docker Containers using:

```
docker pull robertobucher/pysimcoder:latest
```
or
```
docker pull robertobucher/pysimcoder:novnc
```

The first image can be launched with
```
$ docker run --rm --env="DISPLAY" --net=host -v $XAUTHORITY:/tmp/.XAuthority -e XAUTHORITY=/tmp/.XAuthority robertobucher/pysimcoder:latest
```
At the prompt launch
```
psc
```

The second image (pysimcoder:novnc) runs from a web browser:
```
$ docker run --rm -it -p 8080:8080 robertobucher/pysimcoder:novnc
```
Open a browser and go to  `http://<server>:8080/vnc.html`

In the terminal launch
```
psc
```
