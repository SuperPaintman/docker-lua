FROM superpaintman/lua:5.3.3

MAINTAINER superpaintman <superpaintmandeveloper@gmail.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
    unzip \
    && rm -rf /var/lib/apt/lists/*

ENV LUAROCKS_VERSION 2.3.0

RUN curl -SL "https://github.com/keplerproject/luarocks/archive/v$LUAROCKS_VERSION.tar.gz" -o "luarocks-$LUAROCKS_VERSION.tar.gz" \
    && tar -xzvf "luarocks-$LUAROCKS_VERSION.tar.gz" \
    && cd "luarocks-$LUAROCKS_VERSION" \
    && ./configure \
    && make build \
    && make install \
    && cd .. \
    && rm "luarocks-$LUAROCKS_VERSION.tar.gz" \
    && rm -f "pax_global_header" \
    && rm -frd "luarocks-$LUAROCKS_VERSION" \
    && luarocks --version

CMD ["lua"]
