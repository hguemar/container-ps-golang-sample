# Build and run container ps

Initially written for a LinuxCon tutorial, it will be built and run in a docker container.
Then, we mount the Docker daemon socket inside the container where our tool is running.

```bash
# The following steps are commented out because 
# not necessary to run the example
# git clone https://github.com/hguemar/container-ps-golang-sample

# Build the main.go
# docker build -t golang-build -f Dockerfile.build .
# docker run -v $(pwd):/code/ -w /code/ golang-build -o /code/main main.go

# Build the image from scratch
# docker build -t container-ps .

docker run -t -v /var/run/docker.sock:/var/run/docker.sock container-ps
```
