<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:1.8.2rc1`](#eggdrop182rc1)
-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.1`](#eggdrop181)
-	[`eggdrop:stable`](#eggdropstable)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:1.6`](#eggdrop16)
-	[`eggdrop:1.6.21`](#eggdrop1621)

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:bfbf6ed92e885730003aa0ecc69831da851ac1b91b3be37bfbb157c3ec617d76
```

-	Platforms:
	-	linux; amd64

### `eggdrop:develop` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13385742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ab013d5cd60af13131c45d8689170021d2a808a16b8f025e882419bb586619`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:39:21 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Tue, 27 Jun 2017 18:39:45 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 21:10:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 21:10:09 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 21:10:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 11 Jul 2017 19:03:35 GMT
ENV EGGDROP_SHA256=770dbddb4f1d42ecd4f8de0f626f1c5da7f4fa82573d14d4b6fc5083e0b86ab2
# Tue, 11 Jul 2017 19:03:35 GMT
ENV EGGDROP_COMMIT=030cc50e684666da13ed6177d230903c79327a3f
# Tue, 11 Jul 2017 19:04:36 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Tue, 11 Jul 2017 19:04:44 GMT
ENV NICK=
# Tue, 11 Jul 2017 19:04:51 GMT
ENV SERVER=
# Tue, 11 Jul 2017 19:04:58 GMT
ENV LISTEN=3333
# Tue, 11 Jul 2017 19:05:05 GMT
ENV OWNER=
# Tue, 11 Jul 2017 19:05:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 11 Jul 2017 19:05:13 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 11 Jul 2017 19:05:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 11 Jul 2017 19:05:14 GMT
EXPOSE 3333/tcp
# Tue, 11 Jul 2017 19:05:14 GMT
COPY file:d80744926cf822928c4fc2c3f9107364df320eecb3ae407a3a5419a43ae4b872 in /home/eggdrop/eggdrop 
# Tue, 11 Jul 2017 19:05:15 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Tue, 11 Jul 2017 19:05:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 11 Jul 2017 19:05:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32e4a65f3ffa8b2f64ffdb82491dd10a9acd7aac1960956a74bad2483953a6c`  
		Last Modified: Thu, 29 Jun 2017 20:38:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eac8f9ae6f107f767faac9ed278a248b45d29dcd82c4960fd6e3a1b64adf19`  
		Last Modified: Thu, 29 Jun 2017 20:38:16 GMT  
		Size: 7.8 KB (7765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5f14fbcb6e354f21c09e8e8d89d663ebe0c4fb3750077affce46b9e367bcf5`  
		Last Modified: Tue, 11 Jul 2017 19:08:05 GMT  
		Size: 11.4 MB (11403880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317c53ea60b4fb76ec7ed5e3bef90be2ac044124c1957816ddc14213f8885f6`  
		Last Modified: Tue, 11 Jul 2017 19:08:02 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5e326b18e005b103474769cb9ec2bf52346f62128ecd120aa48baf339f66c3`  
		Last Modified: Tue, 11 Jul 2017 19:08:03 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.2rc1`

```console
$ docker pull eggdrop@sha256:b54cf07b3f497f739d14eb605799595d7813566ac6c0003ae8c367a49515a83f
```

-	Platforms:
	-	linux; amd64

### `eggdrop:1.8.2rc1` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9103464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9155e27d37878e2e36785f707af973b59a516438134a34fc437b62d05bdcef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:39:21 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Tue, 27 Jun 2017 18:39:45 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 21:10:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 21:10:09 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 21:10:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 11 Jul 2017 19:06:14 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev  && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.2rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.2rc1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.2rc1.tar.gz.asc eggdrop-1.8.2rc1.tar.gz   && rm eggdrop-1.8.2rc1.tar.gz.asc   && tar -zxvf eggdrop-1.8.2rc1.tar.gz   && rm eggdrop-1.8.2rc1.tar.gz   && ( cd eggdrop-1.8.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Tue, 11 Jul 2017 19:06:24 GMT
ENV NICK=
# Tue, 11 Jul 2017 19:06:31 GMT
ENV SERVER=
# Tue, 11 Jul 2017 19:06:38 GMT
ENV LISTEN=3333
# Tue, 11 Jul 2017 19:06:38 GMT
ENV OWNER=
# Tue, 11 Jul 2017 19:06:45 GMT
ENV USERFILE=eggdrop.user
# Tue, 11 Jul 2017 19:06:52 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 11 Jul 2017 19:06:59 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 11 Jul 2017 19:07:06 GMT
EXPOSE 3333/tcp
# Tue, 11 Jul 2017 19:07:13 GMT
COPY file:ad0e9ec4db3f86e715aedf634680ea8087bc3709bdda493ffcc4d915433e8c35 in /home/eggdrop/eggdrop 
# Tue, 11 Jul 2017 19:07:20 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Tue, 11 Jul 2017 19:07:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 11 Jul 2017 19:07:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32e4a65f3ffa8b2f64ffdb82491dd10a9acd7aac1960956a74bad2483953a6c`  
		Last Modified: Thu, 29 Jun 2017 20:38:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eac8f9ae6f107f767faac9ed278a248b45d29dcd82c4960fd6e3a1b64adf19`  
		Last Modified: Thu, 29 Jun 2017 20:38:16 GMT  
		Size: 7.8 KB (7765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c577c1792353153ec5034b0eeaaa284086c2fc32a04447263b9fe14cd01896c7`  
		Last Modified: Tue, 11 Jul 2017 19:08:24 GMT  
		Size: 7.1 MB (7121609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b241132aed96bde36816a459995c18d3d649cba0802a236c374a0104cce603`  
		Last Modified: Tue, 11 Jul 2017 19:08:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1dce20b3a2991998ad3858f5bed14d94bea457ca13764c62fb4f4a64863c2b`  
		Last Modified: Tue, 11 Jul 2017 19:08:25 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:23d07a07be77f2550357204f144e94a671ed3c94cf946287e631a9c7d9971478
```

-	Platforms:
	-	linux; amd64

### `eggdrop:1.8` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f4df4c38d0f32153594ffafc62f59d27c6fdd12935c51da67fb4fbe649dec2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:55:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 20:55:42 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 20:55:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Jun 2017 21:07:49 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev  && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.1.tar.gz.asc eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz.asc   && tar -zxvf eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz   && ( cd eggdrop-1.8.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Tue, 27 Jun 2017 21:08:12 GMT
ENV NICK=
# Tue, 27 Jun 2017 21:08:13 GMT
ENV SERVER=
# Tue, 27 Jun 2017 21:08:14 GMT
ENV LISTEN=3333
# Tue, 27 Jun 2017 21:08:15 GMT
ENV OWNER=
# Tue, 27 Jun 2017 21:08:16 GMT
ENV USERFILE=eggdrop.user
# Tue, 27 Jun 2017 21:08:41 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 27 Jun 2017 21:08:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 27 Jun 2017 21:08:43 GMT
EXPOSE 3333/tcp
# Tue, 11 Jul 2017 19:07:49 GMT
COPY file:d80744926cf822928c4fc2c3f9107364df320eecb3ae407a3a5419a43ae4b872 in /home/eggdrop/eggdrop 
# Tue, 11 Jul 2017 19:07:50 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Tue, 11 Jul 2017 19:07:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 11 Jul 2017 19:07:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317de5b46aacdce6e9880e6d72fa5b0dafade2ff44ea2f3e5e92dda2db48641`  
		Last Modified: Thu, 29 Jun 2017 20:35:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa8b4aaaf45ddc1747bf091c8974177ce29644d104f6ec4d970a8eb6bf4f79`  
		Last Modified: Thu, 29 Jun 2017 20:35:21 GMT  
		Size: 8.0 KB (8003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3533e40611ab15e65336505f58dff0b1f94707948fb0b425c302bc367c50965f`  
		Last Modified: Thu, 29 Jun 2017 20:36:24 GMT  
		Size: 5.0 MB (4978655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39334fdcfae52d80d02e86fcb277176dd91c00982d1e009787f089cd419db85`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266baec0f84c0bf991b1a9f71267693dfbbffd41990b829bb816d7a4ea9e1b6`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.1`

```console
$ docker pull eggdrop@sha256:23d07a07be77f2550357204f144e94a671ed3c94cf946287e631a9c7d9971478
```

-	Platforms:
	-	linux; amd64

### `eggdrop:1.8.1` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f4df4c38d0f32153594ffafc62f59d27c6fdd12935c51da67fb4fbe649dec2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:55:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 20:55:42 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 20:55:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Jun 2017 21:07:49 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev  && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.1.tar.gz.asc eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz.asc   && tar -zxvf eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz   && ( cd eggdrop-1.8.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Tue, 27 Jun 2017 21:08:12 GMT
ENV NICK=
# Tue, 27 Jun 2017 21:08:13 GMT
ENV SERVER=
# Tue, 27 Jun 2017 21:08:14 GMT
ENV LISTEN=3333
# Tue, 27 Jun 2017 21:08:15 GMT
ENV OWNER=
# Tue, 27 Jun 2017 21:08:16 GMT
ENV USERFILE=eggdrop.user
# Tue, 27 Jun 2017 21:08:41 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 27 Jun 2017 21:08:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 27 Jun 2017 21:08:43 GMT
EXPOSE 3333/tcp
# Tue, 11 Jul 2017 19:07:49 GMT
COPY file:d80744926cf822928c4fc2c3f9107364df320eecb3ae407a3a5419a43ae4b872 in /home/eggdrop/eggdrop 
# Tue, 11 Jul 2017 19:07:50 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Tue, 11 Jul 2017 19:07:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 11 Jul 2017 19:07:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317de5b46aacdce6e9880e6d72fa5b0dafade2ff44ea2f3e5e92dda2db48641`  
		Last Modified: Thu, 29 Jun 2017 20:35:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa8b4aaaf45ddc1747bf091c8974177ce29644d104f6ec4d970a8eb6bf4f79`  
		Last Modified: Thu, 29 Jun 2017 20:35:21 GMT  
		Size: 8.0 KB (8003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3533e40611ab15e65336505f58dff0b1f94707948fb0b425c302bc367c50965f`  
		Last Modified: Thu, 29 Jun 2017 20:36:24 GMT  
		Size: 5.0 MB (4978655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39334fdcfae52d80d02e86fcb277176dd91c00982d1e009787f089cd419db85`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266baec0f84c0bf991b1a9f71267693dfbbffd41990b829bb816d7a4ea9e1b6`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:23d07a07be77f2550357204f144e94a671ed3c94cf946287e631a9c7d9971478
```

-	Platforms:
	-	linux; amd64

### `eggdrop:stable` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f4df4c38d0f32153594ffafc62f59d27c6fdd12935c51da67fb4fbe649dec2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:55:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 20:55:42 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 20:55:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Jun 2017 21:07:49 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev  && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.1.tar.gz.asc eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz.asc   && tar -zxvf eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz   && ( cd eggdrop-1.8.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Tue, 27 Jun 2017 21:08:12 GMT
ENV NICK=
# Tue, 27 Jun 2017 21:08:13 GMT
ENV SERVER=
# Tue, 27 Jun 2017 21:08:14 GMT
ENV LISTEN=3333
# Tue, 27 Jun 2017 21:08:15 GMT
ENV OWNER=
# Tue, 27 Jun 2017 21:08:16 GMT
ENV USERFILE=eggdrop.user
# Tue, 27 Jun 2017 21:08:41 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 27 Jun 2017 21:08:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 27 Jun 2017 21:08:43 GMT
EXPOSE 3333/tcp
# Tue, 11 Jul 2017 19:07:49 GMT
COPY file:d80744926cf822928c4fc2c3f9107364df320eecb3ae407a3a5419a43ae4b872 in /home/eggdrop/eggdrop 
# Tue, 11 Jul 2017 19:07:50 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Tue, 11 Jul 2017 19:07:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 11 Jul 2017 19:07:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317de5b46aacdce6e9880e6d72fa5b0dafade2ff44ea2f3e5e92dda2db48641`  
		Last Modified: Thu, 29 Jun 2017 20:35:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa8b4aaaf45ddc1747bf091c8974177ce29644d104f6ec4d970a8eb6bf4f79`  
		Last Modified: Thu, 29 Jun 2017 20:35:21 GMT  
		Size: 8.0 KB (8003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3533e40611ab15e65336505f58dff0b1f94707948fb0b425c302bc367c50965f`  
		Last Modified: Thu, 29 Jun 2017 20:36:24 GMT  
		Size: 5.0 MB (4978655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39334fdcfae52d80d02e86fcb277176dd91c00982d1e009787f089cd419db85`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266baec0f84c0bf991b1a9f71267693dfbbffd41990b829bb816d7a4ea9e1b6`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:23d07a07be77f2550357204f144e94a671ed3c94cf946287e631a9c7d9971478
```

-	Platforms:
	-	linux; amd64

### `eggdrop:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f4df4c38d0f32153594ffafc62f59d27c6fdd12935c51da67fb4fbe649dec2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:55:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 20:55:42 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 20:55:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Jun 2017 21:07:49 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev  && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.1.tar.gz.asc eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz.asc   && tar -zxvf eggdrop-1.8.1.tar.gz   && rm eggdrop-1.8.1.tar.gz   && ( cd eggdrop-1.8.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Tue, 27 Jun 2017 21:08:12 GMT
ENV NICK=
# Tue, 27 Jun 2017 21:08:13 GMT
ENV SERVER=
# Tue, 27 Jun 2017 21:08:14 GMT
ENV LISTEN=3333
# Tue, 27 Jun 2017 21:08:15 GMT
ENV OWNER=
# Tue, 27 Jun 2017 21:08:16 GMT
ENV USERFILE=eggdrop.user
# Tue, 27 Jun 2017 21:08:41 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 27 Jun 2017 21:08:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 27 Jun 2017 21:08:43 GMT
EXPOSE 3333/tcp
# Tue, 11 Jul 2017 19:07:49 GMT
COPY file:d80744926cf822928c4fc2c3f9107364df320eecb3ae407a3a5419a43ae4b872 in /home/eggdrop/eggdrop 
# Tue, 11 Jul 2017 19:07:50 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Tue, 11 Jul 2017 19:07:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 11 Jul 2017 19:07:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317de5b46aacdce6e9880e6d72fa5b0dafade2ff44ea2f3e5e92dda2db48641`  
		Last Modified: Thu, 29 Jun 2017 20:35:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa8b4aaaf45ddc1747bf091c8974177ce29644d104f6ec4d970a8eb6bf4f79`  
		Last Modified: Thu, 29 Jun 2017 20:35:21 GMT  
		Size: 8.0 KB (8003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3533e40611ab15e65336505f58dff0b1f94707948fb0b425c302bc367c50965f`  
		Last Modified: Thu, 29 Jun 2017 20:36:24 GMT  
		Size: 5.0 MB (4978655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39334fdcfae52d80d02e86fcb277176dd91c00982d1e009787f089cd419db85`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266baec0f84c0bf991b1a9f71267693dfbbffd41990b829bb816d7a4ea9e1b6`  
		Last Modified: Tue, 11 Jul 2017 19:08:50 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.6`

```console
$ docker pull eggdrop@sha256:9d41756bda6ef19c4e0b8f60f5ff169ec11268856a037e3dd27cf7a93e600964
```

-	Platforms:
	-	linux; amd64

### `eggdrop:1.6` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff496560f7da88cae1c64bce9a93f3d87566a7e60544a0dd097af0def90b8e1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:55:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 20:55:42 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 20:55:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Jun 2017 20:56:12 GMT
RUN apk add --no-cache tcl tcl-dev wget make tar gpgme bash build-base   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.6/eggdrop1.6.21.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.6/eggdrop1.6.21.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key B0B3D92ABE1D20233A2ECB01DB909F5EE7C0E7F7   && gpg --batch --verify eggdrop1.6.21.tar.gz.asc eggdrop1.6.21.tar.gz   && rm eggdrop1.6.21.tar.gz.asc   && tar -zxvf eggdrop1.6.21.tar.gz   && rm eggdrop1.6.21.tar.gz   && ( cd eggdrop1.6.21     && CFLAGS="-std=gnu89" ./configure --with-tclinc=/usr/include/tcl.h --with-tcllib=/usr/lib/libtcl8.6.so     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop1.6.21   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget make tar gpgme build-base
# Tue, 27 Jun 2017 21:05:14 GMT
ENV NICK=
# Tue, 27 Jun 2017 21:05:14 GMT
ENV SERVER=
# Tue, 27 Jun 2017 21:05:15 GMT
ENV LISTEN=3333
# Tue, 27 Jun 2017 21:05:40 GMT
ENV OWNER=
# Tue, 27 Jun 2017 21:05:41 GMT
ENV USERFILE=eggdrop.user
# Tue, 27 Jun 2017 21:05:42 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 27 Jun 2017 21:05:43 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 27 Jun 2017 21:06:08 GMT
EXPOSE 3333/tcp
# Mon, 03 Jul 2017 17:51:29 GMT
COPY file:e428f30c058ab0bb09d0e3fa4880f51d23df22141a9f67503ac354e6a71ed388 in /home/eggdrop/eggdrop 
# Mon, 03 Jul 2017 17:51:30 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Mon, 03 Jul 2017 17:51:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Jul 2017 17:51:32 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317de5b46aacdce6e9880e6d72fa5b0dafade2ff44ea2f3e5e92dda2db48641`  
		Last Modified: Thu, 29 Jun 2017 20:35:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa8b4aaaf45ddc1747bf091c8974177ce29644d104f6ec4d970a8eb6bf4f79`  
		Last Modified: Thu, 29 Jun 2017 20:35:21 GMT  
		Size: 8.0 KB (8003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e0891c62b3f2b5ff3f3a64f2d09b7596a6b8071ea712e4df723e4eb9e2e4cf`  
		Last Modified: Thu, 29 Jun 2017 20:35:23 GMT  
		Size: 3.6 MB (3612824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15f1b347335a4e58860171e3680275de00abf91e386e57cfd65c8fb40be68f7`  
		Last Modified: Mon, 03 Jul 2017 17:54:26 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e6823666bb307b4f2e65b1236a5babd80bd02a05c62d377ce5596822d0b8f6`  
		Last Modified: Mon, 03 Jul 2017 17:54:26 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.6.21`

```console
$ docker pull eggdrop@sha256:9d41756bda6ef19c4e0b8f60f5ff169ec11268856a037e3dd27cf7a93e600964
```

-	Platforms:
	-	linux; amd64

### `eggdrop:1.6.21` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff496560f7da88cae1c64bce9a93f3d87566a7e60544a0dd097af0def90b8e1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:55:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 27 Jun 2017 20:55:42 GMT
RUN adduser -S eggdrop
# Tue, 27 Jun 2017 20:55:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Jun 2017 20:56:12 GMT
RUN apk add --no-cache tcl tcl-dev wget make tar gpgme bash build-base   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.6/eggdrop1.6.21.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.6/eggdrop1.6.21.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key B0B3D92ABE1D20233A2ECB01DB909F5EE7C0E7F7   && gpg --batch --verify eggdrop1.6.21.tar.gz.asc eggdrop1.6.21.tar.gz   && rm eggdrop1.6.21.tar.gz.asc   && tar -zxvf eggdrop1.6.21.tar.gz   && rm eggdrop1.6.21.tar.gz   && ( cd eggdrop1.6.21     && CFLAGS="-std=gnu89" ./configure --with-tclinc=/usr/include/tcl.h --with-tcllib=/usr/lib/libtcl8.6.so     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop1.6.21   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget make tar gpgme build-base
# Tue, 27 Jun 2017 21:05:14 GMT
ENV NICK=
# Tue, 27 Jun 2017 21:05:14 GMT
ENV SERVER=
# Tue, 27 Jun 2017 21:05:15 GMT
ENV LISTEN=3333
# Tue, 27 Jun 2017 21:05:40 GMT
ENV OWNER=
# Tue, 27 Jun 2017 21:05:41 GMT
ENV USERFILE=eggdrop.user
# Tue, 27 Jun 2017 21:05:42 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 27 Jun 2017 21:05:43 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 27 Jun 2017 21:06:08 GMT
EXPOSE 3333/tcp
# Mon, 03 Jul 2017 17:51:29 GMT
COPY file:e428f30c058ab0bb09d0e3fa4880f51d23df22141a9f67503ac354e6a71ed388 in /home/eggdrop/eggdrop 
# Mon, 03 Jul 2017 17:51:30 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Mon, 03 Jul 2017 17:51:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Jul 2017 17:51:32 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317de5b46aacdce6e9880e6d72fa5b0dafade2ff44ea2f3e5e92dda2db48641`  
		Last Modified: Thu, 29 Jun 2017 20:35:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa8b4aaaf45ddc1747bf091c8974177ce29644d104f6ec4d970a8eb6bf4f79`  
		Last Modified: Thu, 29 Jun 2017 20:35:21 GMT  
		Size: 8.0 KB (8003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e0891c62b3f2b5ff3f3a64f2d09b7596a6b8071ea712e4df723e4eb9e2e4cf`  
		Last Modified: Thu, 29 Jun 2017 20:35:23 GMT  
		Size: 3.6 MB (3612824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15f1b347335a4e58860171e3680275de00abf91e386e57cfd65c8fb40be68f7`  
		Last Modified: Mon, 03 Jul 2017 17:54:26 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e6823666bb307b4f2e65b1236a5babd80bd02a05c62d377ce5596822d0b8f6`  
		Last Modified: Mon, 03 Jul 2017 17:54:26 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
