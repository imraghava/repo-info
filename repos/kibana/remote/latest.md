## `kibana:latest`

```console
$ docker pull kibana@sha256:953ec76515e924a9b074d01536cfe751260c050718854f4f3e4f475d32d07745
```

-	Platforms:
	-	linux; amd64

### `kibana:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127309449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7c28f22a37bf64b525d1f03f8681ef1e5fcbb714ef69202c7d893eba97acf6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 22:20:05 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 20 Jun 2017 22:20:47 GMT
RUN apt-get update && apt-get install -y 		apt-transport-https 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 20 Jun 2017 22:20:59 GMT
ENV GOSU_VERSION=1.10
# Tue, 20 Jun 2017 22:21:04 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 20 Jun 2017 22:21:27 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 20 Jun 2017 22:21:30 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 20 Jun 2017 22:21:56 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 20 Jun 2017 22:22:20 GMT
RUN echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/kibana.list
# Mon, 10 Jul 2017 17:07:58 GMT
ENV KIBANA_VERSION=5.5.0
# Mon, 10 Jul 2017 17:08:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(server\.host:).*!\2 '0.0.0.0'!" /etc/kibana/kibana.yml 	&& grep -q "^server\.host: '0.0.0.0'\$" /etc/kibana/kibana.yml 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /etc/kibana/kibana.yml 	&& grep -q "^elasticsearch\.url: 'http://elasticsearch:9200'\$" /etc/kibana/kibana.yml
# Mon, 10 Jul 2017 17:08:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Jul 2017 17:08:36 GMT
COPY file:9a3ed3a1655d5afa631fded5211f1c33f5f49f1d1e0e0d9a031c9e8601111f05 in / 
# Mon, 10 Jul 2017 17:08:36 GMT
EXPOSE 5601/tcp
# Mon, 10 Jul 2017 17:08:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Jul 2017 17:08:37 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5f11dcc4056d16ed481272c37a1a39df0c4f23b226e8603df563d03e435967`  
		Last Modified: Tue, 20 Jun 2017 22:31:59 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874bd4f47d7a721a0df4a7647f582f853685cf8e2425963e65284c3a976c8663`  
		Last Modified: Tue, 20 Jun 2017 22:32:05 GMT  
		Size: 22.4 MB (22404961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579b4dc2954d39f3837178bc406754ced3032966f5aa08c0316b55ec3f82b37f`  
		Last Modified: Tue, 20 Jun 2017 22:31:57 GMT  
		Size: 500.7 KB (500661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3da6b03da531ab76e5d529a1989579bf8968b219cd1438691dea3cb329df863`  
		Last Modified: Tue, 20 Jun 2017 22:31:56 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a29671870a29e947d353ea99aadda9177c5d5d4444a40dad7a19b234a7121bb`  
		Last Modified: Tue, 20 Jun 2017 22:31:57 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c52cc60fdec384e6390b7c67c5984ddf5efa62380cae77170bcc0777883631`  
		Last Modified: Tue, 20 Jun 2017 22:31:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d65346dcd831551730cbe7dd3332d6a32094db4d2137c59bc89f781c2db2bd`  
		Last Modified: Mon, 10 Jul 2017 17:09:22 GMT  
		Size: 51.8 MB (51775345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6511d8584b1b63d4656c1a32041b12d35975ba66911b4b37f57445b83ba978b4`  
		Last Modified: Mon, 10 Jul 2017 17:08:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
