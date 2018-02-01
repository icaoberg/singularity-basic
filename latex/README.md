# singularity-ubuntu16.04-latex.simg

![Latex](../images/latex.png)

To create an image using the Singularity definition on this folder, run the commands

```
IMAGE=singularity-ubuntu16.04-latex.simg
DEFINITION=Singularity

singularity image.create -s 5000 $IMAGE
sudo singularity build $IMAGE $DEFINITION
```
