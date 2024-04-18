# Projects Artifacts

# Loading the docker image

Download the file from URL, then load the docker image using the command below:

```
bash
docker load --input image_name.tar

```

## Running the docker image

```bash
docker run --rm --gpus all --ulimit memlock=-1 --ulimit stack=67108864 -v ${PWD}:/workspace -it rep-classkg_image bash


# inside the container, run the required commands

. ./artifact/scripts/run.sh
```

## Issues
- Require multi gpu