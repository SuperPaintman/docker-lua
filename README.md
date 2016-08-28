# Lua

[![Lua][lua-image]][lua-url]


Docker Image packaging for Lua


## Supported tags and respective `Dockerfile` links

* `5.3.3`, `latest` [(Dockerfile)][dockerfile-url]
* `5.3.3-luarocks`, `luarocks` [(luarocks/Dockerfile)][dockerfile-luarocks-url]


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


[lua-image]: README/logo.png
[lua-url]: //www.lua.org
[dockerfile-url]: Dockerfile
[dockerfile-luarocks-url]: luarocks/Dockerfile
