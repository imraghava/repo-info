## `percona:latest`

```console
$ docker pull percona@sha256:6ebcbf3488e2731fdd137a65087f752d026b013bc27983f3c60a234a2fcc94a8
```

-	Platforms:
	-	linux; amd64

### `percona:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128584940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1882f2900392a1d8c67058830919705e1841b15f9598792c792756d56f5bb3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Fri, 23 Jun 2017 00:26:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 23 Jun 2017 00:26:50 GMT
ENV GOSU_VERSION=1.7
# Fri, 23 Jun 2017 00:27:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 23 Jun 2017 00:27:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 23 Jun 2017 00:27:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		apt-transport-https ca-certificates 		pwgen 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jun 2017 02:46:29 GMT
ENV GPG_KEYS=430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	4D1BB29D63D98E422B2113B19334A25F8507EFA5
# Fri, 23 Jun 2017 02:46:32 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/percona.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 23 Jun 2017 02:46:34 GMT
RUN echo 'deb https://repo.percona.com/apt jessie main' > /etc/apt/sources.list.d/percona.list
# Fri, 23 Jun 2017 02:46:35 GMT
ENV PERCONA_MAJOR=5.7
# Fri, 23 Jun 2017 02:46:36 GMT
ENV PERCONA_VERSION=5.7.18-15-1.jessie
# Fri, 23 Jun 2017 02:47:04 GMT
RUN { 		echo percona-server-server-$PERCONA_MAJOR percona-server-server/root_password password 'unused'; 		echo percona-server-server-$PERCONA_MAJOR percona-server-server/root_password_again password 'unused'; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		percona-server-server-$PERCONA_MAJOR=$PERCONA_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 23 Jun 2017 02:47:06 GMT
RUN find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& myCnf="$(find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lE '^\[mysqld\]' 		| head -n1)" 	&& echo 'skip-host-cache\nskip-name-resolve' 		| awk '{ print } $1 == "[mysqld]" && c == 0 { c = 1; system("cat") }' "$myCnf" > /tmp/my.cnf 	&& mv /tmp/my.cnf "$myCnf"
# Fri, 23 Jun 2017 02:47:07 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 23 Jun 2017 02:47:08 GMT
COPY file:01e6982f4616ce5335aa8fc1b158e02657d5596a595c569bb9febb58755d8095 in /usr/local/bin/ 
# Fri, 23 Jun 2017 02:47:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 23 Jun 2017 02:47:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jun 2017 02:47:12 GMT
EXPOSE 3306/tcp
# Fri, 23 Jun 2017 02:47:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e155d2d0e9a4665a3a3fe112e227034275f6e6ea237122a695dbea5a8861`  
		Last Modified: Sat, 24 Jun 2017 12:34:28 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547981b8269f9a3f6be6941c644aa592f59a77e764e0962cacae67e0c6159586`  
		Last Modified: Sat, 24 Jun 2017 12:34:28 GMT  
		Size: 1.3 MB (1304107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9d42ed2f48a29a67c7ce9a017f1b14fabb57f9b7193dd51d39675132b7acc3`  
		Last Modified: Sat, 24 Jun 2017 12:34:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec4aceb5b0f67e929a4da5f441b72d05f4243ad3dc634188c0d99f77ef5eb6`  
		Last Modified: Sat, 24 Jun 2017 12:34:29 GMT  
		Size: 6.7 MB (6671588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0878e8bbf5346824053b50ccd16b9818dd648431ab69571aa7be64a26f843aa9`  
		Last Modified: Sat, 24 Jun 2017 18:45:03 GMT  
		Size: 4.7 KB (4675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be0574f3764db399af8b2cc0f10ce9c70de22a6606cafdc5761aaadc50d84bc`  
		Last Modified: Sat, 24 Jun 2017 18:45:03 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06ffb1ef66c344838357184657d0f9dbf7c92bbd7483d8054ad737a7600733b`  
		Last Modified: Sat, 24 Jun 2017 18:45:18 GMT  
		Size: 68.0 MB (67984391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8a49004a19b57ac33368363ec201a520eb3f73a6348a04fd2d5285159f098c`  
		Last Modified: Sat, 24 Jun 2017 18:45:03 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e62dcab46cc42ed5b22ae488974058fe14e1ae0e6e42e3e7924b924f5b00787`  
		Last Modified: Sat, 24 Jun 2017 18:45:03 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f13103f22b4fb2158ade21ab32959c98bcde9b507700aa8d93e18029d1e22b`  
		Last Modified: Sat, 24 Jun 2017 18:45:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
