## `openjdk:6b38-jdk`

```console
$ docker pull openjdk@sha256:56b88ff75f37a60d2a3aabfc2b647b654e2f026ec7e5132e79069024f0d4d3e8
```

-	Platforms:
	-	linux; amd64

### `openjdk:6b38-jdk` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187302770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d954144b7b01b9c26492ceeea61b61073777edbf51212fd0baab7b9322b62b0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Dec 2016 22:15:37 GMT
ADD file:199da03e20ee14ea6024525caeb8435b86af4b2788f5a8c8f6fb9bb0209f3fff in / 
# Tue, 13 Dec 2016 22:15:46 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:01:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:51:28 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:51:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 13 Dec 2016 23:51:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-6-openjdk-amd64
# Tue, 13 Dec 2016 23:51:30 GMT
ENV JAVA_VERSION=6b38
# Tue, 13 Dec 2016 23:51:30 GMT
ENV JAVA_DEBIAN_VERSION=6b38-1.13.10-1~deb7u1
# Tue, 13 Dec 2016 23:52:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-6-jdk="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
```

-	Layers:
	-	`sha256:b65f3290184628b3ea88b85793900695faa9f3878990fec458a4024dc7211bc5`  
		Last Modified: Tue, 13 Dec 2016 22:26:49 GMT  
		Size: 37.3 MB (37284147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955df57e3a2cd5b72c67014cfd876fd1d7e79c99543be94feb1ae730fb346722`  
		Last Modified: Wed, 14 Dec 2016 03:00:31 GMT  
		Size: 6.8 MB (6823208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bf7f3cec6bd4c967cf5c23c85bd72c1200ab75cb929fde88ea18c387567e7e`  
		Last Modified: Wed, 14 Dec 2016 03:00:42 GMT  
		Size: 37.4 MB (37441906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6905e99379f27bf43285d691575b0a2ee4ff51d6a672da8fa43f4ed3761f677a`  
		Last Modified: Wed, 14 Dec 2016 03:00:24 GMT  
		Size: 413.5 KB (413522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0bafef37530c54bfc436cf6d9c639c47ae51d09bb55fa9fc767fc83e125bb1`  
		Last Modified: Wed, 14 Dec 2016 03:00:23 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8b6415432bd913f6f930550256160ce21b9a8a76ee54212df5f663c0aadf00`  
		Last Modified: Wed, 14 Dec 2016 03:00:55 GMT  
		Size: 105.3 MB (105339745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
