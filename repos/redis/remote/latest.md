## `redis:latest`

```console
$ docker pull redis@sha256:54057dd7e125ca41afe526a877e8bd35ec2cdd33b9217e022ed37bdcf7d09673
```

-	Platforms:
	-	linux; amd64

### `redis:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74246270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2ac2024e4b6d621cea1458923bdbd1806f2c7c50c8a7292e0e6551b8d768e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Nov 2016 20:30:25 GMT
ADD file:41ea5187c50116884c38d9ec51d920d79cfaeb2a61c52e07a97f457419a10a4f in / 
# Mon, 07 Nov 2016 20:30:26 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2016 01:00:56 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 09 Nov 2016 01:01:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 09 Nov 2016 01:01:09 GMT
ENV GOSU_VERSION=1.7
# Wed, 09 Nov 2016 01:01:13 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 06 Dec 2016 22:53:47 GMT
ENV REDIS_VERSION=3.2.6
# Tue, 06 Dec 2016 22:53:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.6.tar.gz
# Tue, 06 Dec 2016 22:53:48 GMT
ENV REDIS_DOWNLOAD_SHA1=0c7bc5c751bdbc6fabed178db9cdbdd948915d1b
# Tue, 06 Dec 2016 22:54:37 GMT
RUN set -ex 		&& buildDeps=' 		gcc 		libc6-dev 		make 	' 	&& apt-get update 	&& apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL" 	&& echo "$REDIS_DOWNLOAD_SHA1 *redis.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/redis 	&& tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1 	&& rm redis.tar.gz 		&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h 	&& sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h 	&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h 		&& make -C /usr/src/redis 	&& make -C /usr/src/redis install 		&& rm -r /usr/src/redis 		&& apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2016 22:54:38 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Dec 2016 22:54:38 GMT
VOLUME [/data]
# Tue, 06 Dec 2016 22:54:39 GMT
WORKDIR /data
# Tue, 06 Dec 2016 22:54:39 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Tue, 06 Dec 2016 22:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2016 22:54:40 GMT
EXPOSE 6379/tcp
# Tue, 06 Dec 2016 22:54:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:386a066cd84a33a04d560c42bef66d1dd64ebfc76de78550e5fd0f8d57778bca`  
		Last Modified: Mon, 07 Nov 2016 20:34:04 GMT  
		Size: 51.4 MB (51356989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769149e3a45cf39c61e1d814263c71759a0c71d2850079ce3ab9ea2512f0dfef`  
		Last Modified: Wed, 09 Nov 2016 01:02:20 GMT  
		Size: 2.0 KB (2044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f43b3c0854aeb84067088fba78133a0dd2f6e358c606d800919b7c0b63f46c9`  
		Last Modified: Wed, 09 Nov 2016 01:02:22 GMT  
		Size: 16.6 MB (16609652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e928127ad85d3e1a54033603b6d4d3408df15fa4c41abc0c8caf6c2d26f07c`  
		Last Modified: Wed, 09 Nov 2016 01:02:18 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0764b5f234259b8396d61d84b1df32afaa6c03333ec9340f54d6410582328e81`  
		Last Modified: Tue, 06 Dec 2016 22:58:17 GMT  
		Size: 5.5 MB (5469156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d40b85d2c524660ef8121f8d74d3167de7e2201b8d2b0c534204997df9d42b`  
		Last Modified: Tue, 06 Dec 2016 22:58:14 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea61cb6ec2a93cc67531451cc701843028e6e1403bb49a217eeebabc834a02d`  
		Last Modified: Tue, 06 Dec 2016 22:58:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
