## `orientdb:latest`

```console
$ docker pull orientdb@sha256:8a6ab8110173e756d8ded7e1e5d5e98d700b98601f53130b8d2cd70dc974c178
```

-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115627284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcfe2351e0f38bd68e2426764874cb6922e7e04c95d9750c7476ea9d303b1bd`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jun 2017 20:03:29 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jun 2017 20:03:30 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 28 Jun 2017 20:04:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 28 Jun 2017 20:04:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 28 Jun 2017 20:04:48 GMT
ENV JAVA_VERSION=8u131
# Wed, 28 Jun 2017 20:04:49 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Wed, 28 Jun 2017 20:04:56 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 28 Jun 2017 20:05:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Jun 2017 20:06:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 11 Jul 2017 17:19:17 GMT
ENV ORIENTDB_VERSION=2.2.23
# Tue, 11 Jul 2017 17:19:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b5876a00eab78237a1098a787b21bed4
# Tue, 11 Jul 2017 17:19:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=33b8a824ac890f7fb5721333e67baa01c2421513
# Tue, 11 Jul 2017 17:19:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.23/orientdb-community-2.2.23.tar.gz
# Tue, 11 Jul 2017 17:19:22 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Tue, 11 Jul 2017 17:19:31 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 11 Jul 2017 17:19:38 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 11 Jul 2017 17:19:39 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 11 Jul 2017 17:19:39 GMT
WORKDIR /orientdb
# Tue, 11 Jul 2017 17:19:40 GMT
EXPOSE 2424/tcp
# Tue, 11 Jul 2017 17:19:41 GMT
EXPOSE 2480/tcp
# Tue, 11 Jul 2017 17:19:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009f6e766a1b230e3ead1ccc615aaa6c631e4683ad31333286adb7be86af61fe`  
		Last Modified: Thu, 29 Jun 2017 23:10:25 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ed68184682c19ccbab7445ae3789b7e8a72ccd4d68b9b64548e0d71c17b15b`  
		Last Modified: Thu, 29 Jun 2017 23:42:08 GMT  
		Size: 70.1 MB (70050180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c4cad53a5d8ed5139732f082adeb5dc0593978a7acecbb77122dcc0a7446a2`  
		Last Modified: Tue, 11 Jul 2017 17:20:39 GMT  
		Size: 646.7 KB (646653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2936d49da1f168ea70652308706fc6e9bbc94f1ceaac83a5f58353bd8076b7`  
		Last Modified: Tue, 11 Jul 2017 17:20:42 GMT  
		Size: 42.9 MB (42939818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
