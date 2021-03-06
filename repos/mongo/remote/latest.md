## `mongo:latest`

```console
$ docker pull mongo@sha256:3f4d30f7f0b256e14bd24df6d931eafb04403f3938792fd17c96075705c18e53
```

-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131637317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c67caab3d8f9ed1fbffe159b10be52e0a0610122c16b3efea50a90ff435584`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 20 Jun 2017 20:14:51 GMT
ADD file:ede5a88363e384813454439a3c2b44c445aea433284d040a20e4149bf9f18a5c in / 
# Tue, 20 Jun 2017 20:14:52 GMT
CMD ["bash"]
# Thu, 22 Jun 2017 20:46:35 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 22 Jun 2017 20:49:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jun 2017 20:49:43 GMT
ENV GOSU_VERSION=1.7
# Thu, 22 Jun 2017 20:49:59 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Thu, 22 Jun 2017 20:50:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jun 2017 20:50:01 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Thu, 22 Jun 2017 20:50:04 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:50:05 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 22 Jun 2017 20:50:05 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:50:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:50:07 GMT
ENV MONGO_MAJOR=3.4
# Thu, 06 Jul 2017 21:55:23 GMT
ENV MONGO_VERSION=3.4.6
# Thu, 06 Jul 2017 21:55:25 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 06 Jul 2017 21:55:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 06 Jul 2017 21:55:45 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 06 Jul 2017 21:55:46 GMT
VOLUME [/data/db /data/configdb]
# Thu, 06 Jul 2017 21:55:48 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Thu, 06 Jul 2017 21:55:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Jul 2017 21:55:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2017 21:55:51 GMT
EXPOSE 27017/tcp
# Thu, 06 Jul 2017 21:55:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f5cc0ee7a6f68b065e4d0a517a2cbae2e3bffb242b3252b53fe77496adaae514`  
		Last Modified: Tue, 20 Jun 2017 20:38:12 GMT  
		Size: 30.1 MB (30130289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99b18c5f0ce9c19f6a53a4fe962536e120578dd2739e500b485bad5aa6b5d8c`  
		Last Modified: Thu, 22 Jun 2017 20:53:43 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abe504e54922f1683c3b7c5bc14d2bb9e5f2199784dd8e3e03fa26e0b8bb02d`  
		Last Modified: Thu, 22 Jun 2017 20:55:02 GMT  
		Size: 2.4 MB (2399182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010336760fd558342d46bcb45fd9e064be8f2e65e3f38cc2fed4e83af3c8f596`  
		Last Modified: Thu, 22 Jun 2017 20:55:01 GMT  
		Size: 881.7 KB (881712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bebc569a09bda60617428252c336fc162f14b774d1233d20e81fd8986ddbab5`  
		Last Modified: Thu, 22 Jun 2017 20:55:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99973eccc29acdec1b2563ebf60ec060afa8b3792e965bfac015abcd364e71bf`  
		Last Modified: Thu, 22 Jun 2017 20:54:58 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c434afa81dd6e165cf36f15cb0b8642b7768e0b28b578428dbe8805d724ed41`  
		Last Modified: Thu, 06 Jul 2017 22:02:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8f112dafbff8fcece795868edff1ca8aef82abd623e0fca8d52f120b6dc698`  
		Last Modified: Thu, 06 Jul 2017 22:02:47 GMT  
		Size: 98.2 MB (98218935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d30b51d2ca2941707417f2b69868225c481b356a772e7fcdcbe22e00a764b8`  
		Last Modified: Thu, 06 Jul 2017 22:02:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6f430709fcf13b0a234ce93277fbf2993ba084215a68cfefedef69e927ef44`  
		Last Modified: Thu, 06 Jul 2017 22:02:21 GMT  
		Size: 3.1 KB (3108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e1ebc5c9671d49401e8cbf5f3e850a085bef573b48dafb36cb399786f15b9f`  
		Last Modified: Thu, 06 Jul 2017 22:02:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
