# pysimCoder_Docker

The two folders contain two versions of Dockerfile for generating two different images of pysimCoder.

![Screenshot_2021-10-31_08-15-46](https://user-images.githubusercontent.com/8348158/139572654-7fc549da-5530-410e-b092-64104a037606.png)

The pysimCoder_X folder contains a Dockerfile that can generate an image that should be run using X support.

It is possible to get both images directly from the Docker Containers using:

```
docker pull robertobucher/pysimcoder:latest
```

Under Windows pysimCoder can be launched with
```
$ docker run --rm -e DISPLAY=<IPADDR>:0.0 --net=host --privileged robertobucher/pysimcoder:latest
```

Under Linux simply use the provided Docker-compose file.

At the prompt launch
```
psc
```

This version contains also the SHV (Silicon-Heaven) tools to modify the parameters of the running RT application on the fly.