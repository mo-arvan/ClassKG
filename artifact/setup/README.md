# Setup

Instructions for creating or organizing the artifacts of a given project. 

## Steps

- Copy the artifacts folder into your projects. 
- Identify the first (or the main) procedure of running the scripts.
- (Optional) If the repository comes with specified requirements, use those.
- Select an appropriate docker image base
- Iteratively run the script that cover missing dependencies, fix bugs, etc.
- Finally, export the docker image to file using the command below `docker save` ()

### Docker
```bash

docker build -t rep-classkg_image -f artifact/setup/dockerfile .




```

### Useful tools

```bash
docker save --output rep-classkg_image.tar rep-classkg_image
split -b 5G rep-classkg_image.tar rep-classkg_image-part-

# inside the container, run the required commands

```

### Useful tools
- `unzip`: `unzip file_name`
- `docker save --output hello-world.tar image_name`