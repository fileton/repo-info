## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:7b952baa7a37b30f0743a70a4415381667cba0c6f5779a13370669b94116437d
```

-	Platforms:
	-	linux; amd64

### `kapacitor:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79509912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711c9fec86a1da8f06dab7ac6c9044d02cf887b4bd9bbe2b7bf6f41f43289ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:06:10 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Wed, 14 Dec 2016 00:57:59 GMT
ENV KAPACITOR_VERSION=1.1.1
# Wed, 14 Dec 2016 00:58:07 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Wed, 14 Dec 2016 00:58:08 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 14 Dec 2016 00:58:08 GMT
EXPOSE 9092/tcp
# Wed, 14 Dec 2016 00:58:09 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 14 Dec 2016 00:58:09 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Wed, 14 Dec 2016 00:58:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Dec 2016 00:58:10 GMT
CMD ["kapacitord"]
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
	-	`sha256:4eb2976d4d206c5b9ac9fc57facba5fa461b15ccbce76a3cd314a77695608545`  
		Last Modified: Mon, 19 Dec 2016 18:17:22 GMT  
		Size: 6.8 KB (6754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770a07eef10046a53cf96b5a3b9bfc8b5491e1b3663900562e38a127f8244f11`  
		Last Modified: Mon, 19 Dec 2016 23:34:42 GMT  
		Size: 9.6 MB (9609596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e868426e5c8c194d3bd192f4cfea5b03de7382267ca8da698dead52eb5974de`  
		Last Modified: Mon, 19 Dec 2016 23:34:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab83f3c6eb8116582e74740a3361faabb0e8ba9bf41c9130cefbf261c162310`  
		Last Modified: Mon, 19 Dec 2016 23:34:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
