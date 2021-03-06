## `redis:32bit`

```console
$ docker pull redis@sha256:02e266ac296a022db559574b0b040c1c7cc54041789014436e0ac130a19182b5
```

-	Platforms:
	-	linux; amd64

### `redis:32bit` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42569592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7583cc66c9f22bd1a90a71c06ea48ccdd0152ace7b29277bcc7889bd28acf5b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 20 Jun 2017 20:14:51 GMT
ADD file:ede5a88363e384813454439a3c2b44c445aea433284d040a20e4149bf9f18a5c in / 
# Tue, 20 Jun 2017 20:14:52 GMT
CMD ["bash"]
# Fri, 23 Jun 2017 05:44:34 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 23 Jun 2017 05:44:35 GMT
ENV GOSU_VERSION=1.10
# Fri, 23 Jun 2017 05:44:57 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 14 Jul 2017 19:50:28 GMT
ENV REDIS_VERSION=4.0.0
# Fri, 14 Jul 2017 19:50:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.0.tar.gz
# Fri, 14 Jul 2017 19:50:29 GMT
ENV REDIS_DOWNLOAD_SHA=d539ae309295721d5c3ed7298939645b6f86ab5d25fdf2a0352ab575c159df2d
# Fri, 14 Jul 2017 19:51:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Jul 2017 19:52:18 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 14 Jul 2017 19:52:19 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 14 Jul 2017 19:52:19 GMT
VOLUME [/data]
# Fri, 14 Jul 2017 19:52:20 GMT
WORKDIR /data
# Fri, 14 Jul 2017 19:52:21 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 14 Jul 2017 19:52:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2017 19:52:22 GMT
EXPOSE 6379/tcp
# Fri, 14 Jul 2017 19:52:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f5cc0ee7a6f68b065e4d0a517a2cbae2e3bffb242b3252b53fe77496adaae514`  
		Last Modified: Tue, 20 Jun 2017 20:38:12 GMT  
		Size: 30.1 MB (30130289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc25ed18e877d43401da85c64188e58d30d84158be61b7c2a380e487c2e7443`  
		Last Modified: Sat, 24 Jun 2017 21:26:11 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e025bc8872f6df52f89826f3bd4300771177bcd0268a5b091bbe11e52d62634d`  
		Last Modified: Sat, 24 Jun 2017 21:26:12 GMT  
		Size: 983.2 KB (983160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bbafe125d9bb51ae1f430cceac55309b3a0c945fdf3aa436f71c0f1146dee3`  
		Last Modified: Fri, 14 Jul 2017 19:55:25 GMT  
		Size: 4.2 MB (4173549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e92ceded42e48e30520c675d679900abbf492d5c01a9cc3a5e93117af1ec`  
		Last Modified: Fri, 14 Jul 2017 19:55:26 GMT  
		Size: 7.3 MB (7280028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733ece64a2667240b23b38f4d7d59bdcd3211cdb90b647a5da1eb2326f285f16`  
		Last Modified: Fri, 14 Jul 2017 19:55:25 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b09043882cce7a3a993169af408fb4b5fe8cc96626b78540879671a20df7f8`  
		Last Modified: Fri, 14 Jul 2017 19:55:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
