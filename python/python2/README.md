# singularity-ubuntu16.04-python2.simg

![Screenshot](../../images/python2.png)

To create an image using the Singularity definition on this folder, run the commands

```
IMAGE=singularity-ubuntu16.04-python2.simg
DEFINITION=Singularity

singularity image.create -s 5000 $IMAGE
sudo singularity build $IMAGE $DEFINITION
```
