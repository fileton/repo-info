## `docker:git`

```console
$ docker pull docker@sha256:f74ccc7f7ad7947ec182d56a67f23073cd4599da95dd30621ef3384be284d4e2
```

-	Platforms:
	-	linux; amd64

### `docker:git` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41179445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20acc36c2dfd417c9bf5168ee372350b5ebdc18ce2de8026aead2ae768456e3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 18 Oct 2016 20:31:22 GMT
ADD file:7afbc23fda8b0b3872623c16af8e3490b2cee951aed14b3794389c2f946cc8c7 in / 
# Tue, 18 Oct 2016 23:04:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Tue, 18 Oct 2016 23:04:50 GMT
ENV DOCKER_BUCKET=get.docker.com
# Mon, 19 Dec 2016 22:08:06 GMT
ENV DOCKER_VERSION=1.12.5
# Mon, 19 Dec 2016 22:08:07 GMT
ENV DOCKER_SHA256=0058867ac46a1eba283e2441b1bb5455df846144f9d9ba079e97655399d4a2c6
# Mon, 19 Dec 2016 22:08:10 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Mon, 19 Dec 2016 22:08:11 GMT
COPY file:a8b1446f032ff01ac092c29a0af328f0b9d47bbee72d1049499f2a9a89ee988a in /usr/local/bin/ 
# Mon, 19 Dec 2016 22:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Dec 2016 22:08:12 GMT
CMD ["sh"]
# Mon, 19 Dec 2016 22:08:22 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:3690ec4760f95690944da86dc4496148a63d85c9e3100669a318110092f6862f`  
		Last Modified: Tue, 18 Oct 2016 20:32:39 GMT  
		Size: 2.3 MB (2312958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601c2ad1cd11213e66512af4a8f4372a4870541b8cf79a9a1058742bf65d6e7`  
		Last Modified: Tue, 18 Oct 2016 23:05:10 GMT  
		Size: 915.1 KB (915061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4778c8461ca643650d385992936097520ca83f0c34899cb445c2e0be8433a9`  
		Last Modified: Mon, 19 Dec 2016 22:12:17 GMT  
		Size: 28.8 MB (28812410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a623eac2dfbff369b20e7b044b473cf5a7c317bd2beea582cc7611ffa4f24a8`  
		Last Modified: Mon, 19 Dec 2016 22:12:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8eccf737966842c2aca739fecbda88e906a1edc3152d303fce1c38e93232fbc`  
		Last Modified: Mon, 19 Dec 2016 22:14:38 GMT  
		Size: 9.1 MB (9138529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
