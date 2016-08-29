FROM buildpack-deps:jessie

MAINTAINER superpaintman <superpaintmandeveloper@gmail.com>

ENV LUA_VERSION 5.2.4

RUN curl -SLO "https://www.lua.org/ftp/lua-$LUA_VERSION.tar.gz" \
    && tar -xzvf "lua-$LUA_VERSION.tar.gz" \
    && cd "lua-$LUA_VERSION" \
    && make linux test \
    && make install \
    && cd .. \
    && rm -frd "lua-$LUA_VERSION" \
    && rm "lua-$LUA_VERSION.tar.gz" \
    && lua -v

CMD ["lua"]
