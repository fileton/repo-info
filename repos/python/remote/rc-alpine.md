## `python:rc-alpine`

```console
$ docker pull python@sha256:c67a91adf3359d9d0f3b27ca974719125a2c5b5a320c010310cc187af832c359
```

-	Platforms:
	-	linux; amd64

### `python:rc-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29392037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c280a16709ddb055ca367c5fe4b7145345c5f5a6d057d83e4e365c7bb67373e`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 18 Oct 2016 20:31:22 GMT
ADD file:7afbc23fda8b0b3872623c16af8e3490b2cee951aed14b3794389c2f946cc8c7 in / 
# Tue, 18 Oct 2016 23:55:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Oct 2016 23:55:28 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2016 23:55:29 GMT
RUN apk add --no-cache ca-certificates
# Wed, 19 Oct 2016 00:05:39 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Mon, 19 Dec 2016 19:23:34 GMT
ENV PYTHON_VERSION=3.6.0rc2
# Mon, 19 Dec 2016 19:23:35 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Mon, 19 Dec 2016 19:25:18 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		gcc 		gdbm-dev 		libc-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& make install 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .python-rundeps $runDeps 	&& apk del .build-deps 	&& rm -rf /usr/src/python ~/.cache
# Mon, 19 Dec 2016 19:25:19 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 19 Dec 2016 19:25:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3690ec4760f95690944da86dc4496148a63d85c9e3100669a318110092f6862f`  
		Last Modified: Tue, 18 Oct 2016 20:32:39 GMT  
		Size: 2.3 MB (2312958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf4eb2be1b3bf382479a4a03e9c969e8ab737697b5abc3d5114705677b9b419`  
		Last Modified: Tue, 18 Oct 2016 23:57:22 GMT  
		Size: 344.0 KB (343957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a807798f510cdf751a07907989373b6ec0a508e93c707132409dee5457b920`  
		Last Modified: Mon, 19 Dec 2016 20:26:45 GMT  
		Size: 26.7 MB (26734861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ad2fb4d8bd9a5ab43f926bb6246b76523a8e44bfaccea68afdac0d96e827c`  
		Last Modified: Mon, 19 Dec 2016 20:26:35 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
