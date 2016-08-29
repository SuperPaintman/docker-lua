# Lua

[![Lua][lua-image]][lua-url]


Docker Image packaging for Lua


## Supported tags and respective `Dockerfile` links

{{DOCKERFILES}}

## How to use this image
### Create a `Dockerfile` in your Lua app project

```Dockerfile
FROM superpaintman/lua:latest
CMD [ "lua", "./your-daemon-or-script.lua" ]
```


You can then build and run the Docker image:

```sh
$ docker build -t my-lua-app .
$ docker run -it --rm --name my-running-app my-lua-app
```


### Run a single Lua script

```sh
$ docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp superpaintman/lua:latest lua your-daemon-or-script.lua
```


[lua-image]: //github.com/SuperPaintman/docker-lua/blob/master/README/logo.png
[lua-url]: //www.lua.org
{{DOCKERFILES_LINKS}}
