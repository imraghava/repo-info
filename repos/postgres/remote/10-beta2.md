## `postgres:10-beta2`

```console
$ docker pull postgres@sha256:1016bd885ded31a763972b16fa7e9a78f1985163e032da18947140d33696a8f1
```

-	Platforms:
	-	linux; amd64

### `postgres:10-beta2` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117430163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff6cf276e81c107d1e00d895bee1a6303e2925994f7fe7625e4c15f46fb0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 Jun 2017 20:24:09 GMT
ADD file:93a0dbb6973bc13e5478292bfe283ff91745ca6e23b6fd3363f0661c45deb1ec in / 
# Tue, 20 Jun 2017 20:24:10 GMT
CMD ["bash"]
# Tue, 27 Jun 2017 17:28:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 27 Jun 2017 17:28:43 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Tue, 27 Jun 2017 17:28:44 GMT
ENV GOSU_VERSION=1.7
# Tue, 27 Jun 2017 17:28:58 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 27 Jun 2017 17:29:04 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 27 Jun 2017 17:29:05 GMT
ENV LANG=en_US.utf8
# Tue, 27 Jun 2017 17:29:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jun 2017 17:29:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jun 2017 17:29:11 GMT
ENV PG_MAJOR=10
# Fri, 14 Jul 2017 22:52:25 GMT
ENV PG_VERSION=10~beta2-1.pgdg90+1
# Fri, 14 Jul 2017 22:52:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' $PG_MAJOR > /etc/apt/sources.list.d/pgdg.list
# Fri, 14 Jul 2017 22:52:49 GMT
RUN apt-get update 	&& apt-get install -y postgresql-common 	&& sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf 	&& apt-get install -y 		postgresql-$PG_MAJOR=$PG_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Jul 2017 22:52:50 GMT
RUN mv -v /usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample /usr/share/postgresql/$PG_MAJOR/ 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Fri, 14 Jul 2017 22:52:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 14 Jul 2017 22:52:52 GMT
ENV PATH=/usr/lib/postgresql/10/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Jul 2017 22:52:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Jul 2017 22:52:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Fri, 14 Jul 2017 22:52:54 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Jul 2017 22:52:55 GMT
COPY file:80a75a207cb3d72777ff2cb8654a6d03754b58aed9199464284f3587637e1403 in /usr/local/bin/ 
# Fri, 14 Jul 2017 22:52:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 14 Jul 2017 22:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2017 22:52:57 GMT
EXPOSE 5432/tcp
# Fri, 14 Jul 2017 22:52:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c75480ad9aafadef6c7faf829ede40cf2fa990c9308d6cd354d53041b01a7cda`  
		Last Modified: Tue, 20 Jun 2017 20:51:29 GMT  
		Size: 45.1 MB (45139825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1c66225faef1d3551f179bd23e48ee3389cf56bc560fc3fbe9ae670766d831`  
		Last Modified: Tue, 27 Jun 2017 17:42:46 GMT  
		Size: 7.0 MB (7029498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbc78e5214f784af25ed88879c709a1074f1f445c293a012735197ea8697d52`  
		Last Modified: Tue, 27 Jun 2017 17:42:44 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70a5244127526a48865363727e72b1cbf0ac29696eb09e25c8c65bd13c5d785`  
		Last Modified: Tue, 27 Jun 2017 17:42:44 GMT  
		Size: 1.3 MB (1276405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a192b6004c2e769747bc8c7e2a3ba7d362c3a9153a8a0962b06a02d958e4faef`  
		Last Modified: Tue, 27 Jun 2017 17:42:45 GMT  
		Size: 6.6 MB (6578940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf364e8a1d670321a8eda1afb1bc7204f9fbf8e3d1f972eea5a93a635ab7a785`  
		Last Modified: Tue, 27 Jun 2017 17:42:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474497d994aec55e796f5b6554f8eea53bf2db439d1eecd74d0e0fa3d936cb3`  
		Last Modified: Tue, 27 Jun 2017 17:42:42 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03616bbbf6d8f94696b3cb9673697f7b594d355d9b453c2103b22bd5379b7d74`  
		Last Modified: Fri, 14 Jul 2017 23:07:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c77e997bbd88ac2da555e0522d551d4c5076f6f4d333ac92e2e593b80d6aff`  
		Last Modified: Fri, 14 Jul 2017 23:07:41 GMT  
		Size: 57.4 MB (57389483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f04e0e482804b405a0a775203efd11acb8bfbf1f0d87317a0918311813a3f29`  
		Last Modified: Fri, 14 Jul 2017 23:07:18 GMT  
		Size: 7.3 KB (7279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8659235916079341745898638dff1e3c5fce2ff06d8d026865d51e20cbacde25`  
		Last Modified: Fri, 14 Jul 2017 23:07:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d374cfb6e19fcf2a10263e23b55cc5f98137d7e0beb787fea9fcb3e8741f130`  
		Last Modified: Fri, 14 Jul 2017 23:07:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccbfa7b9927f875efe03e2eb1880b8da14387ff45b1942e540de2f5892805e6`  
		Last Modified: Fri, 14 Jul 2017 23:07:18 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299dddeb6c54e52fee765ea9b584842dab3456f6b9e4c9ed53e863a2104e3d1a`  
		Last Modified: Fri, 14 Jul 2017 23:07:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
