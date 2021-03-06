## `irssi:debian`

```console
$ docker pull irssi@sha256:3cb43218d5a406e05eec4bafbe974e20ef766ed2e19da7c289e2d457e4837456
```

-	Platforms:
	-	linux; amd64

### `irssi:debian` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95703300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bc95ac436e0160949897f95c404ebaf5231ebf26854d46836d08e97c7f8687`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libglib2.0-0 		libwww-perl 		perl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:50:29 GMT
ENV HOME=/home/user
# Tue, 13 Dec 2016 23:50:30 GMT
RUN useradd --create-home --home-dir $HOME user 	&& mkdir -p $HOME/.irssi 	&& chown -R user:user $HOME
# Tue, 13 Dec 2016 23:50:31 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:50:31 GMT
ENV IRSSI_VERSION=0.8.20
# Tue, 13 Dec 2016 23:51:19 GMT
RUN buildDeps=' 		autoconf 		automake 		bzip2 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		make 		pkg-config 		xz-utils 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz 	&& wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1 	&& gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz 	&& rm -r "$GNUPGHOME" /tmp/irssi.tar.xz.asc 	&& mkdir -p /usr/src/irssi 	&& tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1 	&& rm /tmp/irssi.tar.xz 	&& cd /usr/src/irssi 	&& ./configure 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	&& make -j$(nproc) 	&& make install 	&& rm -rf /usr/src/irssi 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Dec 2016 23:51:19 GMT
WORKDIR /home/user
# Tue, 13 Dec 2016 23:51:20 GMT
VOLUME [/home/user/.irssi]
# Tue, 13 Dec 2016 23:51:20 GMT
USER [user]
# Tue, 13 Dec 2016 23:51:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa21a6fe8bc3f18648d90b3a8b910ad9b21c14f415e17b94f7ada1cae617714`  
		Last Modified: Mon, 19 Dec 2016 23:01:10 GMT  
		Size: 32.3 MB (32262589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c200e6e37b7dd28e68f1dc5ee5e15daba3126e45ee613629b8b3bfc3aef654`  
		Last Modified: Mon, 19 Dec 2016 23:00:56 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b5519e9e63cfbc5e5db2b61b4db8e72b9f6ec44a688885e5e9d05a62d0104b`  
		Last Modified: Mon, 19 Dec 2016 23:01:04 GMT  
		Size: 12.1 MB (12073227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
