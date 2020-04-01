# How to generate Dockerfiles for a new version

If you have GNU `sed` installed on your machine then simply run `make build` after modifying versions in `Makefile`.
Otherwise run `make build` in a Docker container using the following command: 

```console
docker run --rm \
  --volume ${PWD}:/tmp/build \
  --workdir /tmp/build \
  gcc:latest \
  make build
```

To validate the generated Dockerfiles run `make docker-build`.