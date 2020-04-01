# Lua

[![Lua][lua-image]][lua-url]


Docker Image packaging for Lua


## Supported tags and respective `Dockerfile` links

* `5.1.5`, `5.1` [(5.1/Dockerfile)][dockerfile-5.1-url]
* `5.1.5-luarocks`, `5.1-luarocks` [(5.1/Dockerfile)][dockerfile-luarocks-5.1-url]
* `5.2.4`, `5.2` [(5.2/Dockerfile)][dockerfile-5.2-url]
* `5.2.4-luarocks`, `5.2-luarocks` [(5.2/Dockerfile)][dockerfile-luarocks-5.2-url]
* `5.3.5`, `5.3`, `latest` [(5.3/Dockerfile)][dockerfile-5.3-url]
* `5.3.5-luarocks`, `5.3-luarocks`, `luarocks` [(5.3/Dockerfile)][dockerfile-luarocks-5.3-url]


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


[lua-image]: https://raw.githubusercontent.com/SuperPaintman/docker-lua/master/README/logo.png
[lua-url]: //www.lua.org
[dockerfile-5.1-url]: //github.com/SuperPaintman/docker-lua/blob/master/5.1/Dockerfile
[dockerfile-luarocks-5.1-url]: //github.com/SuperPaintman/docker-lua/blob/master/5.1/luarocks/Dockerfile
[dockerfile-5.2-url]: //github.com/SuperPaintman/docker-lua/blob/master/5.2/Dockerfile
[dockerfile-luarocks-5.2-url]: //github.com/SuperPaintman/docker-lua/blob/master/5.2/luarocks/Dockerfile
[dockerfile-5.3-url]: //github.com/SuperPaintman/docker-lua/blob/master/5.3/Dockerfile
[dockerfile-luarocks-5.3-url]: //github.com/SuperPaintman/docker-lua/blob/master/5.3/luarocks/Dockerfile

