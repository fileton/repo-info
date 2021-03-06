## `wordpress:4-php7.0-fpm-alpine`

```console
$ docker pull wordpress@sha256:0592d1796de2bac007b9c8a210c3a6429290a49c7cec4a2e3f4597f35df8f15c
```

-	Platforms:
	-	linux; amd64

### `wordpress:4-php7.0-fpm-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39809701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e5bc0e81a8c294e51eb4014e15eaf385d63f255e9caf46fc97069c251bf8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 18 Oct 2016 20:31:22 GMT
ADD file:7afbc23fda8b0b3872623c16af8e3490b2cee951aed14b3794389c2f946cc8c7 in / 
# Tue, 18 Oct 2016 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 18 Oct 2016 21:17:35 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Tue, 18 Oct 2016 21:17:36 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Tue, 18 Oct 2016 21:17:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Oct 2016 21:17:37 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Tue, 18 Oct 2016 21:28:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Wed, 14 Dec 2016 15:02:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 14 Dec 2016 15:02:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 14 Dec 2016 15:02:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 14 Dec 2016 15:34:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763
# Wed, 14 Dec 2016 15:34:41 GMT
ENV PHP_VERSION=7.0.14
# Wed, 14 Dec 2016 15:34:41 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.14.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.14.tar.xz.asc/from/this/mirror
# Wed, 14 Dec 2016 15:34:41 GMT
ENV PHP_SHA256=0f1dff6392a1cc2ed126b9695f580a2ed77eb09d2c23b41cabfb41e6f27a8c89 PHP_MD5=a51f1d4f03f4e4c745856e9f76fca476
# Wed, 14 Dec 2016 15:34:49 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Wed, 14 Dec 2016 15:34:50 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Wed, 14 Dec 2016 15:38:21 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Wed, 14 Dec 2016 15:38:22 GMT
COPY multi:63f3f133271448127a56d400bfeecd1ab617d6e67215b9f497baf80e5d4550d1 in /usr/local/bin/ 
# Wed, 14 Dec 2016 15:38:22 GMT
WORKDIR /var/www/html
# Wed, 14 Dec 2016 15:38:23 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 14 Dec 2016 15:38:23 GMT
EXPOSE 9000/tcp
# Wed, 14 Dec 2016 15:38:24 GMT
CMD ["php-fpm"]
# Wed, 14 Dec 2016 21:31:24 GMT
RUN apk add --no-cache 		bash 		sed
# Wed, 14 Dec 2016 21:31:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		libjpeg-turbo-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache; 		runDeps="$( 		scanelf --needed --nobanner --recursive 			/usr/local/lib/php/extensions 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Wed, 14 Dec 2016 21:31:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 14 Dec 2016 21:31:59 GMT
VOLUME [/var/www/html]
# Wed, 14 Dec 2016 21:32:00 GMT
ENV WORDPRESS_VERSION=4.7
# Wed, 14 Dec 2016 21:32:00 GMT
ENV WORDPRESS_SHA1=1e14144c4db71421dc4ed22f94c3914dfc3b7020
# Wed, 14 Dec 2016 21:32:03 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Wed, 14 Dec 2016 21:32:04 GMT
COPY file:6e1608064069d6a0efca7e7e6e05498565d1ec00015623fda652cccda073a77b in /usr/local/bin/ 
# Wed, 14 Dec 2016 21:32:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 21:32:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3690ec4760f95690944da86dc4496148a63d85c9e3100669a318110092f6862f`  
		Last Modified: Tue, 18 Oct 2016 20:32:39 GMT  
		Size: 2.3 MB (2312958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67654b7bd8a6f817e849f77cd102331617f4e2394feeae4f77f8683b9b466ed9`  
		Last Modified: Tue, 18 Oct 2016 22:37:25 GMT  
		Size: 1.0 MB (1048149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c453327105c5d394a206069893aa1527b7cc4e58699b4a4b0c2453f5b02a7f`  
		Last Modified: Tue, 18 Oct 2016 22:37:23 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e68959c15a56029b84021fca8cce378aaa0aa08837e08878bbddc694e798c`  
		Last Modified: Tue, 18 Oct 2016 22:37:22 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31899a3a83015655d8ac391ff5382a8e8ac526ebd91c1b45cebe8e570fc039f3`  
		Last Modified: Wed, 14 Dec 2016 16:31:43 GMT  
		Size: 12.7 MB (12707451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038e65afa0ba8c1b7cd42aa5dc23743ee48d39b3287bc15eb49323ccd6f2b890`  
		Last Modified: Wed, 14 Dec 2016 16:31:35 GMT  
		Size: 483.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0083ee24207a752fa385e1acd62ad2fc9a77a00e53f441f4a0557d4114a00a`  
		Last Modified: Wed, 14 Dec 2016 16:31:40 GMT  
		Size: 14.6 MB (14592132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3267ffb508d608d494e8758fa39d5f8c8aaa222f4b59fd23ed6ce5577f34455`  
		Last Modified: Wed, 14 Dec 2016 16:31:35 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc54fab8d039b5b0b214c11d3388d296c88fbd1b172cd460c852b5d0463084d`  
		Last Modified: Wed, 14 Dec 2016 16:31:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863e016f0f6330c4f78db51fcca64946eb4a1bce9a68610369c9c7f0f6e300cf`  
		Last Modified: Wed, 14 Dec 2016 16:31:35 GMT  
		Size: 7.7 KB (7677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0ac2d022d1a9c15b296c1e4f848c8b88dd742e2c760236eec64e692e2a37c0`  
		Last Modified: Wed, 14 Dec 2016 21:44:43 GMT  
		Size: 590.1 KB (590128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fb06c90c33951cdc7cb83399659bd0d064d5bf1ba46e7e2dfd5fb3116b2794`  
		Last Modified: Wed, 14 Dec 2016 21:44:43 GMT  
		Size: 722.0 KB (722044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29552485ddc5a77e6a75162cb2e1f86065e15b8b02e27dd81d7eea7d9da8682`  
		Last Modified: Wed, 14 Dec 2016 21:44:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be3e37e823d99e8099617c0b78ab32b8c10960ac84ec2c2b4b0ebbd3167e4c`  
		Last Modified: Wed, 14 Dec 2016 21:44:45 GMT  
		Size: 7.8 MB (7821948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a8a9264c37961bbbec270e04393c1281f8a7e71acd724ea0230fcabf19417f`  
		Last Modified: Wed, 14 Dec 2016 21:44:43 GMT  
		Size: 2.9 KB (2932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
