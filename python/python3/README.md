# singularity-ubuntu16.04-python3.simg

To build this image use the commands



```
IMAGE=singularity-ubuntu16.04-python3.5.2.simg
DEFINITION=Singularity

singularity image.create -s 5000 $IMAGE
sudo singularity build $IMAGE $DEFINITION
```
