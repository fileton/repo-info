## `sonarqube:lts-alpine`

```console
$ docker pull sonarqube@sha256:92cc02926bb7e01bf8cb7e7865082595ad5a3b63dbe96bc34b7f55866912920b
```

-	Platforms:
	-	linux; amd64

### `sonarqube:lts-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172707227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61625fc49da000f922ace7e9ee3f0a3d97b0daccd07645ee7ede483c611df`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Tue, 18 Oct 2016 20:31:22 GMT
ADD file:7afbc23fda8b0b3872623c16af8e3490b2cee951aed14b3794389c2f946cc8c7 in / 
# Tue, 18 Oct 2016 20:39:57 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2016 20:39:58 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 18 Oct 2016 20:40:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Tue, 18 Oct 2016 20:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 17 Nov 2016 21:47:44 GMT
ENV JAVA_VERSION=8u111
# Thu, 17 Nov 2016 21:47:44 GMT
ENV JAVA_ALPINE_VERSION=8.111.14-r0
# Thu, 17 Nov 2016 21:47:50 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 18 Nov 2016 03:01:18 GMT
MAINTAINER David Gageot <david.gageot@sonarsource.com>
# Tue, 13 Dec 2016 22:11:34 GMT
ENV SONAR_VERSION=5.6.4 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Tue, 13 Dec 2016 22:11:34 GMT
EXPOSE 9000/tcp
# Tue, 13 Dec 2016 22:11:48 GMT
RUN set -x     && apk add --no-cache gnupg unzip curl     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE     && mkdir /opt     && cd /opt     && curl -o sonarqube.zip -fSL https://sonarsource.bintray.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://sonarsource.bintray.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Tue, 13 Dec 2016 22:11:49 GMT
VOLUME [/opt/sonarqube/data]
# Tue, 13 Dec 2016 22:11:49 GMT
WORKDIR /opt/sonarqube
# Tue, 13 Dec 2016 22:11:50 GMT
COPY file:83e169627dc34c4308fd222d47a1ae7c388a283efdc49980a885a8788308a052 in /opt/sonarqube/bin/ 
# Tue, 13 Dec 2016 22:11:51 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:3690ec4760f95690944da86dc4496148a63d85c9e3100669a318110092f6862f`  
		Last Modified: Tue, 18 Oct 2016 20:32:39 GMT  
		Size: 2.3 MB (2312958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdb77eb56b4c44907a822ccdf607323c1f42fd024b7db6be146dd049d95f305`  
		Last Modified: Tue, 18 Oct 2016 20:45:34 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f83c3a978676d457389954188a0d4eae85a2728e4a9ba27f6ec6730e88932fd`  
		Last Modified: Thu, 17 Nov 2016 22:00:11 GMT  
		Size: 49.4 MB (49355709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f2968a1dbf15b445631028d02c040127cf11c860b6cc7e661b2f93ddbdb0f3`  
		Last Modified: Tue, 13 Dec 2016 22:15:24 GMT  
		Size: 121.0 MB (121037900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99585282480f7d38797f4e8b4c22b9faceb17eae906f378de0a66dcdb282e73`  
		Last Modified: Tue, 13 Dec 2016 22:15:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
