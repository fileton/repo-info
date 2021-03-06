<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `thrift`

-	[`thrift:0.9`](#thrift09)
-	[`thrift:0.9.3`](#thrift093)
-	[`thrift:latest`](#thriftlatest)

## `thrift:0.9`

```console
$ docker pull thrift@sha256:8d1c347c92f0c357a780d9578ac266fa5e4c295ef06a8c5ab39909b999587412
```

-	Platforms:
	-	linux; amd64

### `thrift:0.9` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49083172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3706d6843931acf79c7eb5e06df4d23cda089a3cb7e53220c2fc1f01a701e10e`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 07 Nov 2016 20:33:23 GMT
ADD file:6fdd763c7bbd245e1c98a3c937b10dcc9b5383d5d0bcda22e8cbfeb6746932da in / 
# Mon, 07 Nov 2016 20:33:24 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2016 01:40:30 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Wed, 09 Nov 2016 01:40:30 GMT
ENV THRIFT_VERSION=0.9.3
# Wed, 09 Nov 2016 01:43:14 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 09 Nov 2016 01:43:14 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c952bb7239f0af4620e24e9dd88d56be7d4469563f840a911c7721321431d9cb`  
		Last Modified: Mon, 07 Nov 2016 20:42:41 GMT  
		Size: 37.2 MB (37208582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4f31db319ca07e9ff66fafb7d6c8c502f16888822e984fe384eac64308d0ef`  
		Last Modified: Wed, 09 Nov 2016 01:43:31 GMT  
		Size: 11.9 MB (11874590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.9.3`

```console
$ docker pull thrift@sha256:8d1c347c92f0c357a780d9578ac266fa5e4c295ef06a8c5ab39909b999587412
```

-	Platforms:
	-	linux; amd64

### `thrift:0.9.3` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49083172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3706d6843931acf79c7eb5e06df4d23cda089a3cb7e53220c2fc1f01a701e10e`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 07 Nov 2016 20:33:23 GMT
ADD file:6fdd763c7bbd245e1c98a3c937b10dcc9b5383d5d0bcda22e8cbfeb6746932da in / 
# Mon, 07 Nov 2016 20:33:24 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2016 01:40:30 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Wed, 09 Nov 2016 01:40:30 GMT
ENV THRIFT_VERSION=0.9.3
# Wed, 09 Nov 2016 01:43:14 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 09 Nov 2016 01:43:14 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c952bb7239f0af4620e24e9dd88d56be7d4469563f840a911c7721321431d9cb`  
		Last Modified: Mon, 07 Nov 2016 20:42:41 GMT  
		Size: 37.2 MB (37208582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4f31db319ca07e9ff66fafb7d6c8c502f16888822e984fe384eac64308d0ef`  
		Last Modified: Wed, 09 Nov 2016 01:43:31 GMT  
		Size: 11.9 MB (11874590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:latest`

```console
$ docker pull thrift@sha256:8d1c347c92f0c357a780d9578ac266fa5e4c295ef06a8c5ab39909b999587412
```

-	Platforms:
	-	linux; amd64

### `thrift:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49083172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3706d6843931acf79c7eb5e06df4d23cda089a3cb7e53220c2fc1f01a701e10e`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 07 Nov 2016 20:33:23 GMT
ADD file:6fdd763c7bbd245e1c98a3c937b10dcc9b5383d5d0bcda22e8cbfeb6746932da in / 
# Mon, 07 Nov 2016 20:33:24 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2016 01:40:30 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Wed, 09 Nov 2016 01:40:30 GMT
ENV THRIFT_VERSION=0.9.3
# Wed, 09 Nov 2016 01:43:14 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 09 Nov 2016 01:43:14 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c952bb7239f0af4620e24e9dd88d56be7d4469563f840a911c7721321431d9cb`  
		Last Modified: Mon, 07 Nov 2016 20:42:41 GMT  
		Size: 37.2 MB (37208582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4f31db319ca07e9ff66fafb7d6c8c502f16888822e984fe384eac64308d0ef`  
		Last Modified: Wed, 09 Nov 2016 01:43:31 GMT  
		Size: 11.9 MB (11874590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
