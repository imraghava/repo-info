## `cassandra:latest`

```console
$ docker pull cassandra@sha256:b25a30a85b5869257f560fb05296886136b809288f53f32ebefde8967e6e6ca5
```

-	Platforms:
	-	linux; amd64

### `cassandra:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165248790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82d9de5d478077fe5a26f6cd64463bd056ab38a47704bb6a7aa7d0ee8a28225`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 20:13:59 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 21 Jun 2017 00:55:44 GMT
RUN groupadd -r cassandra --gid=999 && useradd -r -g cassandra --uid=999 cassandra
# Wed, 21 Jun 2017 00:55:45 GMT
ENV GOSU_VERSION=1.7
# Wed, 21 Jun 2017 00:56:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 21 Jun 2017 00:56:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libjemalloc1 && rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2017 00:56:28 GMT
RUN { 		echo 'Package: openjdk-* ca-certificates-java'; 		echo 'Pin: release n=*-backports'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/java-backports
# Wed, 21 Jun 2017 00:56:29 GMT
ENV GPG_KEYS=514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA
# Wed, 21 Jun 2017 00:56:32 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/cassandra.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 29 Jun 2017 21:11:45 GMT
RUN echo 'deb http://www.apache.org/dist/cassandra/debian 311x main' >> /etc/apt/sources.list.d/cassandra.list
# Thu, 29 Jun 2017 21:11:46 GMT
ENV CASSANDRA_VERSION=3.11.0
# Thu, 29 Jun 2017 21:13:02 GMT
RUN apt-get update 	&& apt-get install -y 		cassandra="$CASSANDRA_VERSION" 		cassandra-tools="$CASSANDRA_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Thu, 29 Jun 2017 21:13:14 GMT
RUN sed -ri 's/^(JVM_PATCH_VERSION)=.*/\1=25/' /etc/cassandra/cassandra-env.sh
# Thu, 29 Jun 2017 21:13:15 GMT
ENV CASSANDRA_CONFIG=/etc/cassandra
# Thu, 29 Jun 2017 21:13:40 GMT
COPY file:fe6ed91be8debf19da443f09935b578bf6599e644b7a670bf7048d33fb2efa9e in /docker-entrypoint.sh 
# Thu, 29 Jun 2017 21:13:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jun 2017 21:13:43 GMT
RUN mkdir -p /var/lib/cassandra "$CASSANDRA_CONFIG" 	&& chown -R cassandra:cassandra /var/lib/cassandra "$CASSANDRA_CONFIG" 	&& chmod 777 /var/lib/cassandra "$CASSANDRA_CONFIG"
# Thu, 29 Jun 2017 21:13:44 GMT
VOLUME [/var/lib/cassandra]
# Thu, 29 Jun 2017 21:14:10 GMT
EXPOSE 7000/tcp 7001/tcp 7199/tcp 9042/tcp 9160/tcp
# Thu, 29 Jun 2017 21:14:11 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bacf36113fe830a77280f81a8203a228fa4bb4536f145a333709b9da0f7cf7`  
		Last Modified: Tue, 20 Jun 2017 20:37:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6842ab2e6fc74873b3fdee0f94ba55daab8d33d724210c33908cf0851ba7aa`  
		Last Modified: Sat, 24 Jun 2017 06:15:15 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0970d2724fb480b3365da5b7b97433cc584531bdf47f1ca6521872f28118c60`  
		Last Modified: Sat, 24 Jun 2017 06:15:15 GMT  
		Size: 1.3 MB (1304152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd1392a6ce500913c8610a67aee5a0fa60c473187630898271e9414340491b5`  
		Last Modified: Sat, 24 Jun 2017 06:15:15 GMT  
		Size: 172.3 KB (172292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43faf38e08a80fd2c9ca9d6936cc906031c54bef186e9ac81710984b86ae1a50`  
		Last Modified: Sat, 24 Jun 2017 06:15:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a3a082d57197895d5911639f0986dfe53cc0b00248044cac75f78352958e2`  
		Last Modified: Sat, 24 Jun 2017 06:15:12 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7ffe4dc3db58910b5877d0623ffd6a2fc29d47ba63db6e739a44157dafbb04`  
		Last Modified: Thu, 29 Jun 2017 21:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caac33302fe634317b8762e6e02e12ec624f9fd122b1b330ac1b849a8363fa08`  
		Last Modified: Thu, 29 Jun 2017 21:21:52 GMT  
		Size: 111.1 MB (111101472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba01779bed983115f705c70b74d5165abfc56ae81ebdaef60b037350ef5cb95`  
		Last Modified: Thu, 29 Jun 2017 21:21:31 GMT  
		Size: 4.4 KB (4396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa363d655b159a668047db0fe4c09ea51bba1df23aea46059efd873dc1ae416`  
		Last Modified: Thu, 29 Jun 2017 21:21:31 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a5c66a8b99ac43e9422d332673034c58442cd8136a2e0c82a9017d971a30a5`  
		Last Modified: Thu, 29 Jun 2017 21:21:31 GMT  
		Size: 30.0 KB (29971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
