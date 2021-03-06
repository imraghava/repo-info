<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3.0.15`](#mongo3015)
-	[`mongo:3.0`](#mongo30)
-	[`mongo:3.0.15-windowsservercore`](#mongo3015-windowsservercore)
-	[`mongo:3.0-windowsservercore`](#mongo30-windowsservercore)
-	[`mongo:3.2.15`](#mongo3215)
-	[`mongo:3.2`](#mongo32)
-	[`mongo:3.2.15-windowsservercore`](#mongo3215-windowsservercore)
-	[`mongo:3.2-windowsservercore`](#mongo32-windowsservercore)
-	[`mongo:3.4.6`](#mongo346)
-	[`mongo:3.4`](#mongo34)
-	[`mongo:3`](#mongo3)
-	[`mongo:latest`](#mongolatest)
-	[`mongo:3.4.6-windowsservercore`](#mongo346-windowsservercore)
-	[`mongo:3.4-windowsservercore`](#mongo34-windowsservercore)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:windowsservercore`](#mongowindowsservercore)
-	[`mongo:3.5.10`](#mongo3510)
-	[`mongo:3.5`](#mongo35)
-	[`mongo:unstable`](#mongounstable)
-	[`mongo:3.5.10-windowsservercore`](#mongo3510-windowsservercore)
-	[`mongo:3.5-windowsservercore`](#mongo35-windowsservercore)
-	[`mongo:unstable-windowsservercore`](#mongounstable-windowsservercore)

## `mongo:3.0.15`

```console
$ docker pull mongo@sha256:d400d2d9b9873256f22612975a2342e98ee4dd12df884a4a28765a03b167d02e
```

-	Platforms:
	-	linux; amd64

### `mongo:3.0.15` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84441170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf849dcba8141fa313711128767347ec632054341e98e71c1bb70f0ea8971cdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 20 Jun 2017 20:31:15 GMT
ADD file:99d706a1b056666b3cfadb00ebc3fe2bef3f3790d09a14a8a4f349c652aa98b1 in / 
# Tue, 20 Jun 2017 20:31:16 GMT
CMD ["bash"]
# Thu, 22 Jun 2017 20:43:49 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 22 Jun 2017 20:43:51 GMT
RUN echo 'deb http://deb.debian.org/debian wheezy-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 22 Jun 2017 20:44:01 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jun 2017 20:44:02 GMT
ENV GOSU_VERSION=1.7
# Thu, 22 Jun 2017 20:44:12 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Thu, 22 Jun 2017 20:44:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jun 2017 20:44:15 GMT
ENV GPG_KEYS=492EAFE8CD016A07919F1D2B9ECBEC467F0CEB10
# Thu, 22 Jun 2017 20:44:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:44:17 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 22 Jun 2017 20:44:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:44:19 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:44:20 GMT
ENV MONGO_MAJOR=3.0
# Thu, 22 Jun 2017 20:44:21 GMT
ENV MONGO_VERSION=3.0.15
# Thu, 22 Jun 2017 20:44:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian wheezy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 22 Jun 2017 20:44:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 22 Jun 2017 20:44:36 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 22 Jun 2017 20:44:37 GMT
VOLUME [/data/db /data/configdb]
# Thu, 22 Jun 2017 20:44:39 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Thu, 22 Jun 2017 20:44:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jun 2017 20:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jun 2017 20:44:42 GMT
EXPOSE 27017/tcp
# Thu, 22 Jun 2017 20:44:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e905db3f7c950542ae57979a09389fae88fbe10a10d30f30928c3e7d177bf051`  
		Last Modified: Tue, 20 Jun 2017 21:07:00 GMT  
		Size: 19.2 MB (19159206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c3685ad811359a832598f43f781f60600f6541b20cdbb77a735f650043be37`  
		Last Modified: Thu, 22 Jun 2017 20:52:29 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c051db37473387675c36b37b7cf539829d3b981fb1bb7fb001d37f34860dfff9`  
		Last Modified: Thu, 22 Jun 2017 20:52:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b489b1c67f58507bda71c7d71d364ecbe345597b8d7160c5d235cb402bb6ea`  
		Last Modified: Thu, 22 Jun 2017 20:52:29 GMT  
		Size: 2.7 MB (2660802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d10ea76ac8cf571ca5cc7e9d5f62d2341a85728c3618a2928b635a3e964b3cb`  
		Last Modified: Thu, 22 Jun 2017 20:52:28 GMT  
		Size: 914.7 KB (914748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c8f23be6c05f7d28362537266def3df2633b2a05b7c54862c9db35f8ad88f8`  
		Last Modified: Thu, 22 Jun 2017 20:52:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659cdc1d65f820b1702e8394c0e9437e0370810d82d0a7803078c912d229bedb`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9c920d600bcd4f39af3ed807fce2bc5a71d22ababc583a669b8ab98c5738b7`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7097400513248a168f8c73ef58f72d222536805a5abfe5ffdfd978b8218111b`  
		Last Modified: Thu, 22 Jun 2017 20:52:42 GMT  
		Size: 61.7 MB (61698780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350613e9aa6ff7bf835c662bbf0eed9c72affe7f71122a985b23cc7ceba84ac9`  
		Last Modified: Thu, 22 Jun 2017 20:52:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f086828c17d1826e59cbd6b3821cb184dff15c7759feb6a309b89e62e34803`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 3.1 KB (3108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a81c3f4a2d161c544698bf658d90511b6ef39dd09fa76f0348dcc57af286ef`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0`

```console
$ docker pull mongo@sha256:d400d2d9b9873256f22612975a2342e98ee4dd12df884a4a28765a03b167d02e
```

-	Platforms:
	-	linux; amd64

### `mongo:3.0` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84441170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf849dcba8141fa313711128767347ec632054341e98e71c1bb70f0ea8971cdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 20 Jun 2017 20:31:15 GMT
ADD file:99d706a1b056666b3cfadb00ebc3fe2bef3f3790d09a14a8a4f349c652aa98b1 in / 
# Tue, 20 Jun 2017 20:31:16 GMT
CMD ["bash"]
# Thu, 22 Jun 2017 20:43:49 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 22 Jun 2017 20:43:51 GMT
RUN echo 'deb http://deb.debian.org/debian wheezy-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 22 Jun 2017 20:44:01 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jun 2017 20:44:02 GMT
ENV GOSU_VERSION=1.7
# Thu, 22 Jun 2017 20:44:12 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Thu, 22 Jun 2017 20:44:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jun 2017 20:44:15 GMT
ENV GPG_KEYS=492EAFE8CD016A07919F1D2B9ECBEC467F0CEB10
# Thu, 22 Jun 2017 20:44:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:44:17 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 22 Jun 2017 20:44:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:44:19 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:44:20 GMT
ENV MONGO_MAJOR=3.0
# Thu, 22 Jun 2017 20:44:21 GMT
ENV MONGO_VERSION=3.0.15
# Thu, 22 Jun 2017 20:44:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian wheezy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 22 Jun 2017 20:44:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 22 Jun 2017 20:44:36 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 22 Jun 2017 20:44:37 GMT
VOLUME [/data/db /data/configdb]
# Thu, 22 Jun 2017 20:44:39 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Thu, 22 Jun 2017 20:44:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jun 2017 20:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jun 2017 20:44:42 GMT
EXPOSE 27017/tcp
# Thu, 22 Jun 2017 20:44:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e905db3f7c950542ae57979a09389fae88fbe10a10d30f30928c3e7d177bf051`  
		Last Modified: Tue, 20 Jun 2017 21:07:00 GMT  
		Size: 19.2 MB (19159206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c3685ad811359a832598f43f781f60600f6541b20cdbb77a735f650043be37`  
		Last Modified: Thu, 22 Jun 2017 20:52:29 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c051db37473387675c36b37b7cf539829d3b981fb1bb7fb001d37f34860dfff9`  
		Last Modified: Thu, 22 Jun 2017 20:52:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b489b1c67f58507bda71c7d71d364ecbe345597b8d7160c5d235cb402bb6ea`  
		Last Modified: Thu, 22 Jun 2017 20:52:29 GMT  
		Size: 2.7 MB (2660802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d10ea76ac8cf571ca5cc7e9d5f62d2341a85728c3618a2928b635a3e964b3cb`  
		Last Modified: Thu, 22 Jun 2017 20:52:28 GMT  
		Size: 914.7 KB (914748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c8f23be6c05f7d28362537266def3df2633b2a05b7c54862c9db35f8ad88f8`  
		Last Modified: Thu, 22 Jun 2017 20:52:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659cdc1d65f820b1702e8394c0e9437e0370810d82d0a7803078c912d229bedb`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9c920d600bcd4f39af3ed807fce2bc5a71d22ababc583a669b8ab98c5738b7`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7097400513248a168f8c73ef58f72d222536805a5abfe5ffdfd978b8218111b`  
		Last Modified: Thu, 22 Jun 2017 20:52:42 GMT  
		Size: 61.7 MB (61698780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350613e9aa6ff7bf835c662bbf0eed9c72affe7f71122a985b23cc7ceba84ac9`  
		Last Modified: Thu, 22 Jun 2017 20:52:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f086828c17d1826e59cbd6b3821cb184dff15c7759feb6a309b89e62e34803`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 3.1 KB (3108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a81c3f4a2d161c544698bf658d90511b6ef39dd09fa76f0348dcc57af286ef`  
		Last Modified: Thu, 22 Jun 2017 20:52:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0.15-windowsservercore`

```console
$ docker pull mongo@sha256:7a59e60a662838db8e32a324e3c19230904e70c97e2bf9fcb865e7944088ce12
```

-	Platforms:
	-	windows; amd64

### `mongo:3.0.15-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5278975697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9e19b59b4eda8892da2442405afd7659a91ee31a3c5d131057326127bacfc0`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 23 May 2017 22:39:10 GMT
ENV MONGO_VERSION=3.0.15
# Tue, 23 May 2017 22:39:13 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.15-signed.msi
# Tue, 23 May 2017 22:39:15 GMT
ENV MONGO_DOWNLOAD_SHA256=0a10cb87da164df7a1d31180d2ea1f3b096dda6e3d7b9f95c184ef953a1677bb
# Tue, 23 May 2017 22:39:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 23 May 2017 22:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 23 May 2017 22:40:04 GMT
EXPOSE 27017/tcp
# Tue, 23 May 2017 22:40:07 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be41011569f799924864ad0229d7e5468768bc89a4138fa7e761f6d431a1fd6`  
		Last Modified: Tue, 23 May 2017 22:41:46 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a726453c0b90b3f382490c227b2b61d9543d5745dd8792f37dc68f37bc48dcc`  
		Last Modified: Tue, 23 May 2017 22:41:45 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0556eda5a5c1a6a2db1ad79019405b6b32ee4399e7682577efb76e9a2e15d85`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cdcaa5fb0b4620a5deab20dc12840d0dbf58d06c2b9237aa12aed11e4fbac1`  
		Last Modified: Tue, 23 May 2017 22:41:47 GMT  
		Size: 47.1 MB (47079237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835af2fd84ca0c0c00f6b43d340a6fe0c37b73d9ea0f03b907f5022daf85425b`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665e544e76d4f6d90f537dae7944611963b9c69a6b35076a058b3f1c9fa5899a`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f64d66b50da900848bfad55d015a7f6f42baf142a13cf688071c00e74a8fa48`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0-windowsservercore`

```console
$ docker pull mongo@sha256:7a59e60a662838db8e32a324e3c19230904e70c97e2bf9fcb865e7944088ce12
```

-	Platforms:
	-	windows; amd64

### `mongo:3.0-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5278975697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9e19b59b4eda8892da2442405afd7659a91ee31a3c5d131057326127bacfc0`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 23 May 2017 22:39:10 GMT
ENV MONGO_VERSION=3.0.15
# Tue, 23 May 2017 22:39:13 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.15-signed.msi
# Tue, 23 May 2017 22:39:15 GMT
ENV MONGO_DOWNLOAD_SHA256=0a10cb87da164df7a1d31180d2ea1f3b096dda6e3d7b9f95c184ef953a1677bb
# Tue, 23 May 2017 22:39:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 23 May 2017 22:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 23 May 2017 22:40:04 GMT
EXPOSE 27017/tcp
# Tue, 23 May 2017 22:40:07 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be41011569f799924864ad0229d7e5468768bc89a4138fa7e761f6d431a1fd6`  
		Last Modified: Tue, 23 May 2017 22:41:46 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a726453c0b90b3f382490c227b2b61d9543d5745dd8792f37dc68f37bc48dcc`  
		Last Modified: Tue, 23 May 2017 22:41:45 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0556eda5a5c1a6a2db1ad79019405b6b32ee4399e7682577efb76e9a2e15d85`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cdcaa5fb0b4620a5deab20dc12840d0dbf58d06c2b9237aa12aed11e4fbac1`  
		Last Modified: Tue, 23 May 2017 22:41:47 GMT  
		Size: 47.1 MB (47079237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835af2fd84ca0c0c00f6b43d340a6fe0c37b73d9ea0f03b907f5022daf85425b`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665e544e76d4f6d90f537dae7944611963b9c69a6b35076a058b3f1c9fa5899a`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f64d66b50da900848bfad55d015a7f6f42baf142a13cf688071c00e74a8fa48`  
		Last Modified: Tue, 23 May 2017 22:41:37 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2.15`

```console
$ docker pull mongo@sha256:e16881b966c98d013811fb96031d9d79fcaa7f720959935683e393ab8bec2b3f
```

-	Platforms:
	-	linux; amd64

### `mongo:3.2.15` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103954773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a8f127d2135960e4d9b9b996ac90f977f51fbc9d8ecb3e19b5fb778a2c2f72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 20 Jun 2017 20:14:51 GMT
ADD file:ede5a88363e384813454439a3c2b44c445aea433284d040a20e4149bf9f18a5c in / 
# Tue, 20 Jun 2017 20:14:52 GMT
CMD ["bash"]
# Thu, 22 Jun 2017 20:46:35 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 22 Jun 2017 20:46:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates			jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jun 2017 20:46:49 GMT
ENV GOSU_VERSION=1.7
# Thu, 22 Jun 2017 20:47:05 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Thu, 22 Jun 2017 20:47:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jun 2017 20:47:08 GMT
ENV GPG_KEYS=DFFA3DCF326E302C4787673A01C4E7FAAAB2461C 	42F3E95A2C4F08279C4960ADD68FA50FEA312927
# Thu, 22 Jun 2017 20:47:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:47:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 22 Jun 2017 20:47:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:47:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:47:15 GMT
ENV MONGO_MAJOR=3.2
# Mon, 10 Jul 2017 17:29:35 GMT
ENV MONGO_VERSION=3.2.15
# Mon, 10 Jul 2017 17:29:37 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 10 Jul 2017 17:29:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 10 Jul 2017 17:29:56 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 10 Jul 2017 17:29:56 GMT
VOLUME [/data/db /data/configdb]
# Mon, 10 Jul 2017 17:29:57 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Mon, 10 Jul 2017 17:29:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 10 Jul 2017 17:29:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2017 17:29:59 GMT
EXPOSE 27017/tcp
# Mon, 10 Jul 2017 17:29:59 GMT
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
	-	`sha256:6a1f514cd0138484a892e63a7e7aa099f678e405fa4e0fbbc82fc6b7c209e8b9`  
		Last Modified: Thu, 22 Jun 2017 20:53:44 GMT  
		Size: 2.4 MB (2399082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593014b81b1025731e119524f18f85bdc312bd600550d4e718fb1f0f8be3d291`  
		Last Modified: Thu, 22 Jun 2017 20:53:42 GMT  
		Size: 881.7 KB (881745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dda4ea4bc739212f435facda276c90e34f5e696dc79186bbd5728b8f40c18f`  
		Last Modified: Thu, 22 Jun 2017 20:53:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd770a4da9f6ada8da3d0abe1c7760a84fd23e79794c132b5052dddf05ac341d`  
		Last Modified: Thu, 22 Jun 2017 20:53:40 GMT  
		Size: 3.1 KB (3067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40478999a86433400980716ec034d7bd751377588677279d46e5436143f5d33`  
		Last Modified: Mon, 10 Jul 2017 17:30:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97da64e92f984660785219829d8802e83674c860cf3ac9d741cdc961606361fb`  
		Last Modified: Mon, 10 Jul 2017 17:30:45 GMT  
		Size: 70.5 MB (70534826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0395e7ac14098bca00a0e0dc079e84e7318931322ba85a4085c704b3f2c2a980`  
		Last Modified: Mon, 10 Jul 2017 17:30:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd14b2c0b0ec3e7853725522c55a4a56e076e5a2026a45533c1c5a782e098ad`  
		Last Modified: Mon, 10 Jul 2017 17:30:30 GMT  
		Size: 3.1 KB (3108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985703d1d0d24fc269813231b7bec7c9a5923c2fee2ada91afb0fc8226a44a51`  
		Last Modified: Mon, 10 Jul 2017 17:30:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2`

```console
$ docker pull mongo@sha256:e16881b966c98d013811fb96031d9d79fcaa7f720959935683e393ab8bec2b3f
```

-	Platforms:
	-	linux; amd64

### `mongo:3.2` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103954773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a8f127d2135960e4d9b9b996ac90f977f51fbc9d8ecb3e19b5fb778a2c2f72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 20 Jun 2017 20:14:51 GMT
ADD file:ede5a88363e384813454439a3c2b44c445aea433284d040a20e4149bf9f18a5c in / 
# Tue, 20 Jun 2017 20:14:52 GMT
CMD ["bash"]
# Thu, 22 Jun 2017 20:46:35 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 22 Jun 2017 20:46:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates			jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jun 2017 20:46:49 GMT
ENV GOSU_VERSION=1.7
# Thu, 22 Jun 2017 20:47:05 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Thu, 22 Jun 2017 20:47:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jun 2017 20:47:08 GMT
ENV GPG_KEYS=DFFA3DCF326E302C4787673A01C4E7FAAAB2461C 	42F3E95A2C4F08279C4960ADD68FA50FEA312927
# Thu, 22 Jun 2017 20:47:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:47:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 22 Jun 2017 20:47:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:47:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:47:15 GMT
ENV MONGO_MAJOR=3.2
# Mon, 10 Jul 2017 17:29:35 GMT
ENV MONGO_VERSION=3.2.15
# Mon, 10 Jul 2017 17:29:37 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 10 Jul 2017 17:29:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 10 Jul 2017 17:29:56 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 10 Jul 2017 17:29:56 GMT
VOLUME [/data/db /data/configdb]
# Mon, 10 Jul 2017 17:29:57 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Mon, 10 Jul 2017 17:29:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 10 Jul 2017 17:29:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2017 17:29:59 GMT
EXPOSE 27017/tcp
# Mon, 10 Jul 2017 17:29:59 GMT
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
	-	`sha256:6a1f514cd0138484a892e63a7e7aa099f678e405fa4e0fbbc82fc6b7c209e8b9`  
		Last Modified: Thu, 22 Jun 2017 20:53:44 GMT  
		Size: 2.4 MB (2399082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593014b81b1025731e119524f18f85bdc312bd600550d4e718fb1f0f8be3d291`  
		Last Modified: Thu, 22 Jun 2017 20:53:42 GMT  
		Size: 881.7 KB (881745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dda4ea4bc739212f435facda276c90e34f5e696dc79186bbd5728b8f40c18f`  
		Last Modified: Thu, 22 Jun 2017 20:53:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd770a4da9f6ada8da3d0abe1c7760a84fd23e79794c132b5052dddf05ac341d`  
		Last Modified: Thu, 22 Jun 2017 20:53:40 GMT  
		Size: 3.1 KB (3067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40478999a86433400980716ec034d7bd751377588677279d46e5436143f5d33`  
		Last Modified: Mon, 10 Jul 2017 17:30:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97da64e92f984660785219829d8802e83674c860cf3ac9d741cdc961606361fb`  
		Last Modified: Mon, 10 Jul 2017 17:30:45 GMT  
		Size: 70.5 MB (70534826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0395e7ac14098bca00a0e0dc079e84e7318931322ba85a4085c704b3f2c2a980`  
		Last Modified: Mon, 10 Jul 2017 17:30:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd14b2c0b0ec3e7853725522c55a4a56e076e5a2026a45533c1c5a782e098ad`  
		Last Modified: Mon, 10 Jul 2017 17:30:30 GMT  
		Size: 3.1 KB (3108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985703d1d0d24fc269813231b7bec7c9a5923c2fee2ada91afb0fc8226a44a51`  
		Last Modified: Mon, 10 Jul 2017 17:30:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2.15-windowsservercore`

```console
$ docker pull mongo@sha256:fe56a401238349a669735ae199e423a4bd8c85ee5e46c6f38eee289f8c13583d
```

-	Platforms:
	-	windows; amd64

### `mongo:3.2.15-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5284935584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f186224c8ec97581ba60bac40e3e4771b2b0c0c7c27f76c4bc4f74c500ba9e`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jul 2017 18:25:54 GMT
ENV MONGO_VERSION=3.2.15
# Wed, 12 Jul 2017 18:25:57 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.2.15-signed.msi
# Wed, 12 Jul 2017 18:25:59 GMT
ENV MONGO_DOWNLOAD_SHA256=e70c38121de2718993702a50b657f3f5bc850d3267e816caf1e5fcc5d6842da0
# Wed, 12 Jul 2017 18:26:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jul 2017 18:26:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jul 2017 18:26:47 GMT
EXPOSE 27017/tcp
# Wed, 12 Jul 2017 18:26:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c04ab9a63da82aaa177e3235179b2e28d6b0189f042f813c476f7da0e92cf`  
		Last Modified: Wed, 12 Jul 2017 19:01:55 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab0ae4976afa93deecd56ad9199c2f6a7d38a421c463e0ecdb0a26e02500cd5`  
		Last Modified: Wed, 12 Jul 2017 19:01:53 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02811ae378ef2194397fd3da356d704276092f93cab722fa6c25c3b5ad1861b1`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb9162c78c3d253458c338a06ed38dd61535f6ca02e97b1b52399e24ab021b1`  
		Last Modified: Wed, 12 Jul 2017 19:01:57 GMT  
		Size: 53.0 MB (53039088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdd5c1b38b5aa8c1d7b4409a7a29e391637fef12d1d92bee047972718389cae`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf02413a9a739e1b573b62e60c7028948001150b8d58ebbef0e7c2d11b969a25`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473f4f0df946814ee7c9e7c006506d6b6b4cb2137a7c3094a1e1efc6617176d2`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2-windowsservercore`

```console
$ docker pull mongo@sha256:fe56a401238349a669735ae199e423a4bd8c85ee5e46c6f38eee289f8c13583d
```

-	Platforms:
	-	windows; amd64

### `mongo:3.2-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5284935584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f186224c8ec97581ba60bac40e3e4771b2b0c0c7c27f76c4bc4f74c500ba9e`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jul 2017 18:25:54 GMT
ENV MONGO_VERSION=3.2.15
# Wed, 12 Jul 2017 18:25:57 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.2.15-signed.msi
# Wed, 12 Jul 2017 18:25:59 GMT
ENV MONGO_DOWNLOAD_SHA256=e70c38121de2718993702a50b657f3f5bc850d3267e816caf1e5fcc5d6842da0
# Wed, 12 Jul 2017 18:26:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jul 2017 18:26:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jul 2017 18:26:47 GMT
EXPOSE 27017/tcp
# Wed, 12 Jul 2017 18:26:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c04ab9a63da82aaa177e3235179b2e28d6b0189f042f813c476f7da0e92cf`  
		Last Modified: Wed, 12 Jul 2017 19:01:55 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab0ae4976afa93deecd56ad9199c2f6a7d38a421c463e0ecdb0a26e02500cd5`  
		Last Modified: Wed, 12 Jul 2017 19:01:53 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02811ae378ef2194397fd3da356d704276092f93cab722fa6c25c3b5ad1861b1`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb9162c78c3d253458c338a06ed38dd61535f6ca02e97b1b52399e24ab021b1`  
		Last Modified: Wed, 12 Jul 2017 19:01:57 GMT  
		Size: 53.0 MB (53039088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdd5c1b38b5aa8c1d7b4409a7a29e391637fef12d1d92bee047972718389cae`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf02413a9a739e1b573b62e60c7028948001150b8d58ebbef0e7c2d11b969a25`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473f4f0df946814ee7c9e7c006506d6b6b4cb2137a7c3094a1e1efc6617176d2`  
		Last Modified: Wed, 12 Jul 2017 19:01:46 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.6`

```console
$ docker pull mongo@sha256:3f4d30f7f0b256e14bd24df6d931eafb04403f3938792fd17c96075705c18e53
```

-	Platforms:
	-	linux; amd64

### `mongo:3.4.6` - linux; amd64

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

## `mongo:3.4`

```console
$ docker pull mongo@sha256:3f4d30f7f0b256e14bd24df6d931eafb04403f3938792fd17c96075705c18e53
```

-	Platforms:
	-	linux; amd64

### `mongo:3.4` - linux; amd64

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

## `mongo:3`

```console
$ docker pull mongo@sha256:3f4d30f7f0b256e14bd24df6d931eafb04403f3938792fd17c96075705c18e53
```

-	Platforms:
	-	linux; amd64

### `mongo:3` - linux; amd64

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

## `mongo:3.4.6-windowsservercore`

```console
$ docker pull mongo@sha256:88c61669fc3ce78e9ffd85b6fb73689bece1bc763362be9fb75580945c7237ff
```

-	Platforms:
	-	windows; amd64

### `mongo:3.4.6-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5295110311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f999d1d3b2f383e7dcd79870afbbcfefd4e38fb46c0e9dc7cfe7ca2e5f9a1`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 06 Jul 2017 21:28:28 GMT
ENV MONGO_VERSION=3.4.6
# Thu, 06 Jul 2017 21:28:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.6-signed.msi
# Thu, 06 Jul 2017 21:28:32 GMT
ENV MONGO_DOWNLOAD_SHA256=c02704728c40d50c66e3d3c3b1e4c27dc70cbe67722e28c7f537cba05f98309c
# Thu, 06 Jul 2017 21:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 06 Jul 2017 21:29:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 06 Jul 2017 21:29:43 GMT
EXPOSE 27017/tcp
# Thu, 06 Jul 2017 21:29:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e6caf6fe4fa11de28c95e118ac04fcf7e7515358e0c5bb6875a3e867b8002e`  
		Last Modified: Thu, 06 Jul 2017 21:30:18 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5689863418539dd972ed5a2fe14455cb308828d4ada7814d257e82d64ebc0815`  
		Last Modified: Thu, 06 Jul 2017 21:30:17 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78d4f89ebca82d28bd53ab156f99b0cc7a1281f01cdf359c88479df04c5a8e`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855eade9a2bdc45a873550e0cbd11e8511aa06352934ea1837a3601a4323f604`  
		Last Modified: Thu, 06 Jul 2017 21:30:21 GMT  
		Size: 63.2 MB (63213840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5907429ed4b12c9c8feb90f5119da7fae90b8de79cccefb4708fde9db7834`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ee4bc56e0638bfeb4913bcfcc932dba6420aaacea6484a886f8a5351f9ebf`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ceb13c71f454610e64520e9c87cbdf0da48b6fe4c24a829dace8968ff25120`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4-windowsservercore`

```console
$ docker pull mongo@sha256:88c61669fc3ce78e9ffd85b6fb73689bece1bc763362be9fb75580945c7237ff
```

-	Platforms:
	-	windows; amd64

### `mongo:3.4-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5295110311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f999d1d3b2f383e7dcd79870afbbcfefd4e38fb46c0e9dc7cfe7ca2e5f9a1`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 06 Jul 2017 21:28:28 GMT
ENV MONGO_VERSION=3.4.6
# Thu, 06 Jul 2017 21:28:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.6-signed.msi
# Thu, 06 Jul 2017 21:28:32 GMT
ENV MONGO_DOWNLOAD_SHA256=c02704728c40d50c66e3d3c3b1e4c27dc70cbe67722e28c7f537cba05f98309c
# Thu, 06 Jul 2017 21:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 06 Jul 2017 21:29:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 06 Jul 2017 21:29:43 GMT
EXPOSE 27017/tcp
# Thu, 06 Jul 2017 21:29:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e6caf6fe4fa11de28c95e118ac04fcf7e7515358e0c5bb6875a3e867b8002e`  
		Last Modified: Thu, 06 Jul 2017 21:30:18 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5689863418539dd972ed5a2fe14455cb308828d4ada7814d257e82d64ebc0815`  
		Last Modified: Thu, 06 Jul 2017 21:30:17 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78d4f89ebca82d28bd53ab156f99b0cc7a1281f01cdf359c88479df04c5a8e`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855eade9a2bdc45a873550e0cbd11e8511aa06352934ea1837a3601a4323f604`  
		Last Modified: Thu, 06 Jul 2017 21:30:21 GMT  
		Size: 63.2 MB (63213840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5907429ed4b12c9c8feb90f5119da7fae90b8de79cccefb4708fde9db7834`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ee4bc56e0638bfeb4913bcfcc932dba6420aaacea6484a886f8a5351f9ebf`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ceb13c71f454610e64520e9c87cbdf0da48b6fe4c24a829dace8968ff25120`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:88c61669fc3ce78e9ffd85b6fb73689bece1bc763362be9fb75580945c7237ff
```

-	Platforms:
	-	windows; amd64

### `mongo:3-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5295110311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f999d1d3b2f383e7dcd79870afbbcfefd4e38fb46c0e9dc7cfe7ca2e5f9a1`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 06 Jul 2017 21:28:28 GMT
ENV MONGO_VERSION=3.4.6
# Thu, 06 Jul 2017 21:28:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.6-signed.msi
# Thu, 06 Jul 2017 21:28:32 GMT
ENV MONGO_DOWNLOAD_SHA256=c02704728c40d50c66e3d3c3b1e4c27dc70cbe67722e28c7f537cba05f98309c
# Thu, 06 Jul 2017 21:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 06 Jul 2017 21:29:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 06 Jul 2017 21:29:43 GMT
EXPOSE 27017/tcp
# Thu, 06 Jul 2017 21:29:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e6caf6fe4fa11de28c95e118ac04fcf7e7515358e0c5bb6875a3e867b8002e`  
		Last Modified: Thu, 06 Jul 2017 21:30:18 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5689863418539dd972ed5a2fe14455cb308828d4ada7814d257e82d64ebc0815`  
		Last Modified: Thu, 06 Jul 2017 21:30:17 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78d4f89ebca82d28bd53ab156f99b0cc7a1281f01cdf359c88479df04c5a8e`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855eade9a2bdc45a873550e0cbd11e8511aa06352934ea1837a3601a4323f604`  
		Last Modified: Thu, 06 Jul 2017 21:30:21 GMT  
		Size: 63.2 MB (63213840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5907429ed4b12c9c8feb90f5119da7fae90b8de79cccefb4708fde9db7834`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ee4bc56e0638bfeb4913bcfcc932dba6420aaacea6484a886f8a5351f9ebf`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ceb13c71f454610e64520e9c87cbdf0da48b6fe4c24a829dace8968ff25120`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:88c61669fc3ce78e9ffd85b6fb73689bece1bc763362be9fb75580945c7237ff
```

-	Platforms:
	-	windows; amd64

### `mongo:windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5295110311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f999d1d3b2f383e7dcd79870afbbcfefd4e38fb46c0e9dc7cfe7ca2e5f9a1`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 06 Jul 2017 21:28:28 GMT
ENV MONGO_VERSION=3.4.6
# Thu, 06 Jul 2017 21:28:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.6-signed.msi
# Thu, 06 Jul 2017 21:28:32 GMT
ENV MONGO_DOWNLOAD_SHA256=c02704728c40d50c66e3d3c3b1e4c27dc70cbe67722e28c7f537cba05f98309c
# Thu, 06 Jul 2017 21:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 06 Jul 2017 21:29:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 06 Jul 2017 21:29:43 GMT
EXPOSE 27017/tcp
# Thu, 06 Jul 2017 21:29:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e6caf6fe4fa11de28c95e118ac04fcf7e7515358e0c5bb6875a3e867b8002e`  
		Last Modified: Thu, 06 Jul 2017 21:30:18 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5689863418539dd972ed5a2fe14455cb308828d4ada7814d257e82d64ebc0815`  
		Last Modified: Thu, 06 Jul 2017 21:30:17 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78d4f89ebca82d28bd53ab156f99b0cc7a1281f01cdf359c88479df04c5a8e`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855eade9a2bdc45a873550e0cbd11e8511aa06352934ea1837a3601a4323f604`  
		Last Modified: Thu, 06 Jul 2017 21:30:21 GMT  
		Size: 63.2 MB (63213840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5907429ed4b12c9c8feb90f5119da7fae90b8de79cccefb4708fde9db7834`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ee4bc56e0638bfeb4913bcfcc932dba6420aaacea6484a886f8a5351f9ebf`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ceb13c71f454610e64520e9c87cbdf0da48b6fe4c24a829dace8968ff25120`  
		Last Modified: Thu, 06 Jul 2017 21:30:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5.10`

```console
$ docker pull mongo@sha256:64af6902d60626c0ecdda1ee8952fb3c08e62262b9e5fd716e1af405be483185
```

-	Platforms:
	-	linux; amd64

### `mongo:3.5.10` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129816939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a78858ab3fe0af467b8f5617be2f73aae132ba26a130dd7ae1114021cb78d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod","--bind_ip_all"]`

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
# Thu, 22 Jun 2017 20:51:22 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Thu, 22 Jun 2017 20:51:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:51:26 GMT
ARG MONGO_PACKAGE=mongodb-org-unstable
# Thu, 22 Jun 2017 20:51:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:51:27 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:51:28 GMT
ENV MONGO_MAJOR=3.5
# Thu, 13 Jul 2017 17:43:01 GMT
ENV MONGO_VERSION=3.5.10
# Thu, 13 Jul 2017 17:43:02 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 13 Jul 2017 17:43:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 13 Jul 2017 17:43:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 13 Jul 2017 17:43:29 GMT
VOLUME [/data/db /data/configdb]
# Thu, 13 Jul 2017 17:43:30 GMT
COPY file:2693b7d26a4d17558bb637a0ad2c43c3be68788377b0e9eb105cd67726d4b645 in /usr/local/bin/ 
# Thu, 13 Jul 2017 17:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2017 17:43:31 GMT
EXPOSE 27017/tcp
# Thu, 13 Jul 2017 17:43:31 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:4b9e8d47828ff0174cadb0a3e8ef6124f2ec31a5b323ed40ed64f752a5814357`  
		Last Modified: Thu, 22 Jun 2017 20:57:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9dc71043104f78db940e403defdbda0695270a65e1ea1f571adeeb37f9e603`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db0cc23eb66b67b4cb77b69742e0e564f16d012b20a8b6804030951e63517ae`  
		Last Modified: Thu, 13 Jul 2017 17:45:39 GMT  
		Size: 96.4 MB (96398615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f82e067a22537683165731b5a66009fce6f110963fab59a5b32d0ceabb7a22`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364c7356976233f5b1b9715d93905591d6297cf83e37424fec9b973287336209`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 3.2 KB (3170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5`

```console
$ docker pull mongo@sha256:64af6902d60626c0ecdda1ee8952fb3c08e62262b9e5fd716e1af405be483185
```

-	Platforms:
	-	linux; amd64

### `mongo:3.5` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129816939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a78858ab3fe0af467b8f5617be2f73aae132ba26a130dd7ae1114021cb78d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod","--bind_ip_all"]`

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
# Thu, 22 Jun 2017 20:51:22 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Thu, 22 Jun 2017 20:51:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:51:26 GMT
ARG MONGO_PACKAGE=mongodb-org-unstable
# Thu, 22 Jun 2017 20:51:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:51:27 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:51:28 GMT
ENV MONGO_MAJOR=3.5
# Thu, 13 Jul 2017 17:43:01 GMT
ENV MONGO_VERSION=3.5.10
# Thu, 13 Jul 2017 17:43:02 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 13 Jul 2017 17:43:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 13 Jul 2017 17:43:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 13 Jul 2017 17:43:29 GMT
VOLUME [/data/db /data/configdb]
# Thu, 13 Jul 2017 17:43:30 GMT
COPY file:2693b7d26a4d17558bb637a0ad2c43c3be68788377b0e9eb105cd67726d4b645 in /usr/local/bin/ 
# Thu, 13 Jul 2017 17:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2017 17:43:31 GMT
EXPOSE 27017/tcp
# Thu, 13 Jul 2017 17:43:31 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:4b9e8d47828ff0174cadb0a3e8ef6124f2ec31a5b323ed40ed64f752a5814357`  
		Last Modified: Thu, 22 Jun 2017 20:57:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9dc71043104f78db940e403defdbda0695270a65e1ea1f571adeeb37f9e603`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db0cc23eb66b67b4cb77b69742e0e564f16d012b20a8b6804030951e63517ae`  
		Last Modified: Thu, 13 Jul 2017 17:45:39 GMT  
		Size: 96.4 MB (96398615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f82e067a22537683165731b5a66009fce6f110963fab59a5b32d0ceabb7a22`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364c7356976233f5b1b9715d93905591d6297cf83e37424fec9b973287336209`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 3.2 KB (3170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:unstable`

```console
$ docker pull mongo@sha256:64af6902d60626c0ecdda1ee8952fb3c08e62262b9e5fd716e1af405be483185
```

-	Platforms:
	-	linux; amd64

### `mongo:unstable` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129816939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a78858ab3fe0af467b8f5617be2f73aae132ba26a130dd7ae1114021cb78d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod","--bind_ip_all"]`

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
# Thu, 22 Jun 2017 20:51:22 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Thu, 22 Jun 2017 20:51:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jun 2017 20:51:26 GMT
ARG MONGO_PACKAGE=mongodb-org-unstable
# Thu, 22 Jun 2017 20:51:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:51:27 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable MONGO_REPO=repo.mongodb.org
# Thu, 22 Jun 2017 20:51:28 GMT
ENV MONGO_MAJOR=3.5
# Thu, 13 Jul 2017 17:43:01 GMT
ENV MONGO_VERSION=3.5.10
# Thu, 13 Jul 2017 17:43:02 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 13 Jul 2017 17:43:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 13 Jul 2017 17:43:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 13 Jul 2017 17:43:29 GMT
VOLUME [/data/db /data/configdb]
# Thu, 13 Jul 2017 17:43:30 GMT
COPY file:2693b7d26a4d17558bb637a0ad2c43c3be68788377b0e9eb105cd67726d4b645 in /usr/local/bin/ 
# Thu, 13 Jul 2017 17:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2017 17:43:31 GMT
EXPOSE 27017/tcp
# Thu, 13 Jul 2017 17:43:31 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:4b9e8d47828ff0174cadb0a3e8ef6124f2ec31a5b323ed40ed64f752a5814357`  
		Last Modified: Thu, 22 Jun 2017 20:57:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9dc71043104f78db940e403defdbda0695270a65e1ea1f571adeeb37f9e603`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db0cc23eb66b67b4cb77b69742e0e564f16d012b20a8b6804030951e63517ae`  
		Last Modified: Thu, 13 Jul 2017 17:45:39 GMT  
		Size: 96.4 MB (96398615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f82e067a22537683165731b5a66009fce6f110963fab59a5b32d0ceabb7a22`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364c7356976233f5b1b9715d93905591d6297cf83e37424fec9b973287336209`  
		Last Modified: Thu, 13 Jul 2017 17:45:12 GMT  
		Size: 3.2 KB (3170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5.10-windowsservercore`

```console
$ docker pull mongo@sha256:b66d2e7a931a249beeb09439fd554a23f7169af7b66a21932d9a35478cb1df95
```

-	Platforms:
	-	windows; amd64

### `mongo:3.5.10-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5300504125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8485775c1b9f736e0e61d7ac9ed5538da35ba1a3d8daa22b489db7bdaef248c1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Jul 2017 17:37:46 GMT
ENV MONGO_VERSION=3.5.10
# Thu, 13 Jul 2017 17:37:49 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.5.10-signed.msi
# Thu, 13 Jul 2017 17:37:51 GMT
ENV MONGO_DOWNLOAD_SHA256=c40ae817a47c2ca07c5f6aca2139a485af7d253e47a5a802eb085057ae6c86d5
# Thu, 13 Jul 2017 17:40:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Jul 2017 17:40:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Jul 2017 17:40:08 GMT
EXPOSE 27017/tcp
# Thu, 13 Jul 2017 17:40:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0d91ab2c7e2b94e154dc6e01ae406d6eee53c143bfee41761e3d9a19b049`  
		Last Modified: Thu, 13 Jul 2017 17:40:53 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1837c75d4de8d99abd099ae9fdcab833cea0f1121bd378d36fe5a0f3e29408ba`  
		Last Modified: Thu, 13 Jul 2017 17:40:51 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de627065e0823590c4ccad762a991abfa452862dd74fba7455eb0672ca23a1`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d84113d04222f851c929c6831a3b4721d7026b1c2045caaec55b90786b4b7d`  
		Last Modified: Thu, 13 Jul 2017 17:40:57 GMT  
		Size: 68.6 MB (68607656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c225975a9033796be1719b72a5032619404be34f44724b02e859821bc8184a`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad0594821d10cd1214c9b4e317ad8931707d3a86ee2645f4df201944829066f`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9158f59419379605ad03f178d8eaa829caf8e36aff8a44403b8f4961090cafdf`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5-windowsservercore`

```console
$ docker pull mongo@sha256:b66d2e7a931a249beeb09439fd554a23f7169af7b66a21932d9a35478cb1df95
```

-	Platforms:
	-	windows; amd64

### `mongo:3.5-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5300504125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8485775c1b9f736e0e61d7ac9ed5538da35ba1a3d8daa22b489db7bdaef248c1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Jul 2017 17:37:46 GMT
ENV MONGO_VERSION=3.5.10
# Thu, 13 Jul 2017 17:37:49 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.5.10-signed.msi
# Thu, 13 Jul 2017 17:37:51 GMT
ENV MONGO_DOWNLOAD_SHA256=c40ae817a47c2ca07c5f6aca2139a485af7d253e47a5a802eb085057ae6c86d5
# Thu, 13 Jul 2017 17:40:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Jul 2017 17:40:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Jul 2017 17:40:08 GMT
EXPOSE 27017/tcp
# Thu, 13 Jul 2017 17:40:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0d91ab2c7e2b94e154dc6e01ae406d6eee53c143bfee41761e3d9a19b049`  
		Last Modified: Thu, 13 Jul 2017 17:40:53 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1837c75d4de8d99abd099ae9fdcab833cea0f1121bd378d36fe5a0f3e29408ba`  
		Last Modified: Thu, 13 Jul 2017 17:40:51 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de627065e0823590c4ccad762a991abfa452862dd74fba7455eb0672ca23a1`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d84113d04222f851c929c6831a3b4721d7026b1c2045caaec55b90786b4b7d`  
		Last Modified: Thu, 13 Jul 2017 17:40:57 GMT  
		Size: 68.6 MB (68607656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c225975a9033796be1719b72a5032619404be34f44724b02e859821bc8184a`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad0594821d10cd1214c9b4e317ad8931707d3a86ee2645f4df201944829066f`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9158f59419379605ad03f178d8eaa829caf8e36aff8a44403b8f4961090cafdf`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:unstable-windowsservercore`

```console
$ docker pull mongo@sha256:b66d2e7a931a249beeb09439fd554a23f7169af7b66a21932d9a35478cb1df95
```

-	Platforms:
	-	windows; amd64

### `mongo:unstable-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5300504125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8485775c1b9f736e0e61d7ac9ed5538da35ba1a3d8daa22b489db7bdaef248c1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Tue, 18 Apr 2017 17:08:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Jul 2017 17:37:46 GMT
ENV MONGO_VERSION=3.5.10
# Thu, 13 Jul 2017 17:37:49 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.5.10-signed.msi
# Thu, 13 Jul 2017 17:37:51 GMT
ENV MONGO_DOWNLOAD_SHA256=c40ae817a47c2ca07c5f6aca2139a485af7d253e47a5a802eb085057ae6c86d5
# Thu, 13 Jul 2017 17:40:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Jul 2017 17:40:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Jul 2017 17:40:08 GMT
EXPOSE 27017/tcp
# Thu, 13 Jul 2017 17:40:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2869ce7d2a7c3a942c84de08ac9b045cb0a8deefa17949b571dffa5cd1cc28cd`  
		Last Modified: Tue, 18 Apr 2017 17:14:24 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0d91ab2c7e2b94e154dc6e01ae406d6eee53c143bfee41761e3d9a19b049`  
		Last Modified: Thu, 13 Jul 2017 17:40:53 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1837c75d4de8d99abd099ae9fdcab833cea0f1121bd378d36fe5a0f3e29408ba`  
		Last Modified: Thu, 13 Jul 2017 17:40:51 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de627065e0823590c4ccad762a991abfa452862dd74fba7455eb0672ca23a1`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d84113d04222f851c929c6831a3b4721d7026b1c2045caaec55b90786b4b7d`  
		Last Modified: Thu, 13 Jul 2017 17:40:57 GMT  
		Size: 68.6 MB (68607656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c225975a9033796be1719b72a5032619404be34f44724b02e859821bc8184a`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad0594821d10cd1214c9b4e317ad8931707d3a86ee2645f4df201944829066f`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9158f59419379605ad03f178d8eaa829caf8e36aff8a44403b8f4961090cafdf`  
		Last Modified: Thu, 13 Jul 2017 17:40:44 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
