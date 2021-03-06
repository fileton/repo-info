## `nuxeo:latest`

```console
$ docker pull nuxeo@sha256:54c69d6c452a71df8a6ac4bc50f90874e7060ae54bd85252db97f48afab05c8f
```

-	Platforms:
	-	linux; amd64

### `nuxeo:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.3 MB (711292858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef2ae64bac9a5ebc28f6edbd0494821b12467d9ca82b18475639f178bcf901f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:52:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:54:12 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 13 Dec 2016 23:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:54:13 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 13 Dec 2016 23:54:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
# Tue, 13 Dec 2016 23:54:14 GMT
ENV JAVA_VERSION=8u111
# Tue, 13 Dec 2016 23:54:14 GMT
ENV JAVA_DEBIAN_VERSION=8u111-b14-2~bpo8+1
# Tue, 13 Dec 2016 23:54:15 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20140324
# Tue, 13 Dec 2016 23:54:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 13 Dec 2016 23:55:00 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 14 Dec 2016 03:32:28 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 14 Dec 2016 03:32:29 GMT
ENV NUXEO_USER=nuxeo
# Wed, 14 Dec 2016 03:32:30 GMT
RUN useradd -m -d /home/$NUXEO_USER -s /bin/bash $NUXEO_USER
# Wed, 14 Dec 2016 03:32:30 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 14:01:09 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 14 Dec 2016 14:02:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 14:02:47 GMT
ENV NUXEO_VERSION=8.10
# Wed, 14 Dec 2016 14:02:47 GMT
ENV NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Wed, 14 Dec 2016 14:02:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 14 Dec 2016 14:03:09 GMT
RUN curl -fsSL "http://cdn.nuxeo.com/nuxeo-${NUXEO_VERSION}/nuxeo-server-${NUXEO_VERSION}-tomcat.zip" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Wed, 14 Dec 2016 14:03:10 GMT
RUN mkdir /docker-entrypoint-initnuxeo.d
# Wed, 14 Dec 2016 14:03:10 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2016 14:03:11 GMT
WORKDIR /opt/nuxeo/server
# Wed, 14 Dec 2016 14:03:11 GMT
COPY file:5cebeee78434ce067bd4b8b9c42eaa20349f1a252aaf628add51d12663b04917 in / 
# Wed, 14 Dec 2016 14:03:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Dec 2016 14:03:12 GMT
EXPOSE 8080/tcp
# Wed, 14 Dec 2016 14:03:12 GMT
EXPOSE 8787/tcp
# Wed, 14 Dec 2016 14:03:13 GMT
CMD ["nuxeoctl" "console"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de64c72267e88e952b064236cb906c7626f7c07a1a2d5900cf6953e72632b3`  
		Last Modified: Wed, 14 Dec 2016 03:04:38 GMT  
		Size: 18.5 MB (18529983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4306be1e8943b446026b96c2ef7b3ab8471c760774fd1cd11334df7084fed57b`  
		Last Modified: Wed, 14 Dec 2016 03:04:50 GMT  
		Size: 42.5 MB (42502002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6944bfb7182c4b1f546a4bcd888d00bdb92bb016bde7d243af3712549534d9`  
		Last Modified: Wed, 14 Dec 2016 03:04:28 GMT  
		Size: 593.4 KB (593384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3521f2f45ed2f586ef5e6423f3dc3f4e36f7460007c2827b827131d2254ecc44`  
		Last Modified: Wed, 14 Dec 2016 03:11:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2f0d9b5f90c348276759c85fae2d52adae563fad53786e8e99862eb3aeab90`  
		Last Modified: Wed, 14 Dec 2016 03:11:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cedcf6d25273f360503909554028b54a92d914805ed9d834cbe31e8ebfeb923`  
		Last Modified: Wed, 14 Dec 2016 03:12:30 GMT  
		Size: 130.1 MB (130108711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f99da7583d58b782d9a4c14ef448bf6f6771e15a7975a2450111ed0a34b381`  
		Last Modified: Wed, 14 Dec 2016 03:11:34 GMT  
		Size: 284.2 KB (284180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21ab7d84051bcfb6a8c0844dcbee32c36f0e2c7c231a4518a3e92c079e31376`  
		Last Modified: Wed, 14 Dec 2016 20:53:29 GMT  
		Size: 4.4 KB (4400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ac55dab447f0675d1bee8660aa101f9c6fc20e1a83474248eb14ec5106078b`  
		Last Modified: Wed, 14 Dec 2016 20:53:27 GMT  
		Size: 807.9 KB (807928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451d514ac41acb7bc176c58e033bc08e0277eb7fa6c5ed7c9b7685179e6a7e0b`  
		Last Modified: Wed, 14 Dec 2016 20:54:30 GMT  
		Size: 197.6 MB (197559482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725374343d4037da9354acab42d803035bc195b26a73dfed7ab4a1f51940e9f9`  
		Last Modified: Wed, 14 Dec 2016 20:54:52 GMT  
		Size: 269.5 MB (269537568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdfcb06637e3c3aa8c30c24ec6150d23fb227f3cf3814c28564fd936889a968`  
		Last Modified: Wed, 14 Dec 2016 20:53:26 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89b1fbaf8e64eb2d771d0184cbfa046c216ff3c817731ab3b85616596e81c30`  
		Last Modified: Wed, 14 Dec 2016 20:53:26 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
