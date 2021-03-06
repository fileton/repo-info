## `redmine:latest`

```console
$ docker pull redmine@sha256:f58d722656a28181a604864b69c62f52eb96032888831063d95295b500d1081c
```

-	Platforms:
	-	linux; amd64

### `redmine:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245953839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18ceb02a6ff2fba4d9f1f853c1cfcda2512b528334fd4e7db5cc4b7f0de2677`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:29:34 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 19:29:35 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 14 Dec 2016 19:35:00 GMT
ENV RUBY_MAJOR=2.2
# Wed, 14 Dec 2016 19:35:01 GMT
ENV RUBY_VERSION=2.2.6
# Wed, 14 Dec 2016 19:35:01 GMT
ENV RUBY_DOWNLOAD_SHA256=de8e192791cb157d610c48a9a9ff6e7f19d67ce86052feae62b82e3682cc675f
# Wed, 14 Dec 2016 19:35:01 GMT
ENV RUBYGEMS_VERSION=2.6.8
# Wed, 14 Dec 2016 19:37:33 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.gz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& ./configure --disable-install-doc --enable-shared 	&& make -j"$(nproc)" 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION"
# Wed, 14 Dec 2016 19:37:34 GMT
ENV BUNDLER_VERSION=1.13.6
# Wed, 14 Dec 2016 19:37:35 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Wed, 14 Dec 2016 19:37:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Dec 2016 19:37:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Dec 2016 19:37:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2016 19:37:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Wed, 14 Dec 2016 19:37:37 GMT
CMD ["irb"]
# Mon, 19 Dec 2016 17:15:10 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Mon, 19 Dec 2016 17:15:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 19 Dec 2016 17:15:25 GMT
ENV GOSU_VERSION=1.7
# Mon, 19 Dec 2016 17:15:30 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Mon, 19 Dec 2016 17:15:30 GMT
ENV TINI_VERSION=v0.9.0
# Mon, 19 Dec 2016 17:15:32 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Mon, 19 Dec 2016 17:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Mon, 19 Dec 2016 17:16:04 GMT
ENV RAILS_ENV=production
# Mon, 19 Dec 2016 17:16:05 GMT
WORKDIR /usr/src/redmine
# Mon, 19 Dec 2016 17:16:05 GMT
ENV REDMINE_VERSION=3.3.1
# Mon, 19 Dec 2016 17:16:05 GMT
ENV REDMINE_DOWNLOAD_MD5=cb8aab3e03cae7d21d003a307e51c176
# Mon, 19 Dec 2016 17:16:09 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Mon, 19 Dec 2016 17:18:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Mon, 19 Dec 2016 17:19:02 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 19 Dec 2016 17:19:03 GMT
COPY file:aff587ea4827aab52eb00cbff38d8d409b101320f09f8ac6545d538ba4ed8f4f in / 
# Mon, 19 Dec 2016 17:19:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Dec 2016 17:19:03 GMT
EXPOSE 3000/tcp
# Mon, 19 Dec 2016 17:19:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f214bcc245dd5c26f327f40bd86b0e8b4ce9e6844b9f4853af727fbe3ae27`  
		Last Modified: Mon, 19 Dec 2016 23:23:29 GMT  
		Size: 10.0 MB (9981063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b0f7b75b7bfe530be21a60de20b1480905a2ad4149ee21b945900c39a40751`  
		Last Modified: Mon, 19 Dec 2016 23:23:21 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50db5958fd3a21284388f26fab47d0cb1250f0809d78ccac437364e4d542a9b`  
		Last Modified: Mon, 19 Dec 2016 23:23:36 GMT  
		Size: 33.3 MB (33278876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3522489202ca97da167a76842dac8d2ae6c3e657f102f7b66bd476afd476e0d3`  
		Last Modified: Mon, 19 Dec 2016 23:23:16 GMT  
		Size: 612.6 KB (612613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65031a5ab0488c71810b02280beeefc0664c11e17e518a90fbcb39be4b716fe`  
		Last Modified: Mon, 19 Dec 2016 23:23:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d45dd7d6fdcbd9e57640d3b2bf4191a54df4cfe12e989a05e546d1a56e45a52`  
		Last Modified: Mon, 19 Dec 2016 23:23:13 GMT  
		Size: 2.0 KB (2041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bff0d846da3b0c325ac64d79935e87a0aa58abd4fb9674c6791864d5c427ce`  
		Last Modified: Mon, 19 Dec 2016 23:23:17 GMT  
		Size: 13.9 MB (13863686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e80df52c77340ba80d5b19c2dbe4bfbac4c854125dbc3b1ec61d1df9360d67`  
		Last Modified: Mon, 19 Dec 2016 23:23:10 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82360e69c13e603e72cd86a629d8ee02a17506902efb65a556784fbd7b3c707`  
		Last Modified: Mon, 19 Dec 2016 23:23:10 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2ca5a6751983a7dbcfee84f4538f4960abd909836880086a03f2144be6da67`  
		Last Modified: Mon, 19 Dec 2016 23:23:36 GMT  
		Size: 58.2 MB (58199191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e67dc6a630c95f3a6b16f1927532a14032927992395e5a80cdfc887c3b8445`  
		Last Modified: Mon, 19 Dec 2016 23:23:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6373378e5a211b9d3dfc703e9dbf4c9bd6b5c2b45bc95efba4dc086d5732fdc3`  
		Last Modified: Mon, 19 Dec 2016 23:27:02 GMT  
		Size: 2.4 MB (2372941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf4a3d4ea85c4e20de20ca357b3c7a3b2bbd9f91ca39d9ed18f1a52b61f26d`  
		Last Modified: Mon, 19 Dec 2016 23:27:19 GMT  
		Size: 75.5 MB (75463291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7035873c7abd5bff2e8bd32494874d3997c0937c39b6bf783c5ce92daafc4ae`  
		Last Modified: Mon, 19 Dec 2016 23:26:59 GMT  
		Size: 1.5 KB (1459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
