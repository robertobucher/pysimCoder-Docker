# pysimCoder from a bash
 
Launch the docker image using
```
$ docker run --rm --env="DISPLAY" --net=host -v $XAUTHORITY:/tmp/.XAuthority -e XAUTHORITY=/tmp/.XAuthority --privileged robertobucher/pysimcoder:latest
```
At the prompt launch
```
psc
```

This version include the Silikon-Heaven application to modify the parameters of the RT task during the execution.


