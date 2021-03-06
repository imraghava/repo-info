## `redis:alpine`

```console
$ docker pull redis@sha256:67c6760513424f2512fd47912b3d21183e989f9299cc158f53fac37571e427e6
```

-	Platforms:
	-	linux; amd64

### `redis:alpine` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10462401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fedae67fbf45fed9997bce664141f225ff931373b11c6095131339fe4afd4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jun 2017 22:13:58 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 28 Jun 2017 22:14:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 14 Jul 2017 19:52:30 GMT
ENV REDIS_VERSION=4.0.0
# Fri, 14 Jul 2017 19:52:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.0.tar.gz
# Fri, 14 Jul 2017 19:52:32 GMT
ENV REDIS_DOWNLOAD_SHA=d539ae309295721d5c3ed7298939645b6f86ab5d25fdf2a0352ab575c159df2d
# Fri, 14 Jul 2017 19:52:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Fri, 14 Jul 2017 19:52:59 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 14 Jul 2017 19:53:00 GMT
VOLUME [/data]
# Fri, 14 Jul 2017 19:53:01 GMT
WORKDIR /data
# Fri, 14 Jul 2017 19:53:01 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Fri, 14 Jul 2017 19:53:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2017 19:53:03 GMT
EXPOSE 6379/tcp
# Fri, 14 Jul 2017 19:53:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b1ac6c7a5068201d8b63a09bb15358ec1616b813ef3942eb8cc12ae191227f`  
		Last Modified: Fri, 30 Jun 2017 00:51:24 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e2e140ea27b3e89f359cd9fab4ec45647dda2a8e5fb0c78633217d9dca87b5`  
		Last Modified: Fri, 30 Jun 2017 00:51:24 GMT  
		Size: 8.2 KB (8164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1045fb5418a5367a45bbc3a40f8f9b0667de9304e07ba36425a43d80a1fb461`  
		Last Modified: Fri, 14 Jul 2017 19:56:10 GMT  
		Size: 8.5 MB (8462095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6857b28dd4359a6307366c6d8ba765d0c668c535fe4545b0512cf2fb299eeeaf`  
		Last Modified: Fri, 14 Jul 2017 19:56:09 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4c40a02aad1514cfe4fd43a187ce2624e9b1135ffd6f012e7c876c73bbe572`  
		Last Modified: Fri, 14 Jul 2017 19:56:08 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
