# pysimCoder_Docker

The two folders contain two Docker for generating two different images of pysimCoder.

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

