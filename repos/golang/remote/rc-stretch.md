## `golang:rc-stretch`

```console
$ docker pull golang@sha256:8e2de5072c0eb7aeaa9734bb60bd3a105f09302fdcce76368b9f894be383ef37
```

-	Platforms:
	-	linux; amd64

### `golang:rc-stretch` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266681781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5741ccbb20a83c0696f1c9e181a6e007efc9cf4533777095c660bbc05e64dd5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Jan 2017 20:39:16 GMT
ADD file:c09931042d44875d1db95d3faa08303a098dfc42738c80d38856cb84d78ebbda in / 
# Mon, 16 Jan 2017 20:39:24 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:01:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 00:02:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2017 18:51:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2017 18:51:43 GMT
ENV GOLANG_VERSION=1.8rc3
# Fri, 10 Feb 2017 18:51:43 GMT
ENV GOLANG_DOWNLOAD_URL=https://golang.org/dl/go1.8rc3.linux-amd64.tar.gz
# Fri, 10 Feb 2017 18:51:43 GMT
ENV GOLANG_DOWNLOAD_SHA256=0ff3faba02ac83920a65b453785771e75f128fbf9ba4ad1d5e72c044103f9c7a
# Fri, 10 Feb 2017 18:51:55 GMT
RUN curl -fsSL "$GOLANG_DOWNLOAD_URL" -o golang.tar.gz 	&& echo "$GOLANG_DOWNLOAD_SHA256  golang.tar.gz" | sha256sum -c - 	&& tar -C /usr/local -xzf golang.tar.gz 	&& rm golang.tar.gz
# Fri, 10 Feb 2017 18:51:56 GMT
ENV GOPATH=/go
# Fri, 10 Feb 2017 18:51:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Feb 2017 18:51:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 10 Feb 2017 18:51:57 GMT
WORKDIR /go
# Fri, 10 Feb 2017 18:51:58 GMT
COPY file:f6191f2c86edc9343569339f101facba47e886e33e29d70da6916ca6b1101a53 in /usr/local/bin/ 
```

-	Layers:
	-	`sha256:cdc4502972ee4dbc3dbcc16a2eeaddaa8179f090379768f8cb9438cd01bf5d8a`  
		Last Modified: Mon, 16 Jan 2017 20:50:09 GMT  
		Size: 43.9 MB (43871389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f85d83d587c9dffea05a7552cfb010c9d4124a626e61dfa27649b01ce06bb6`  
		Last Modified: Tue, 17 Jan 2017 00:22:42 GMT  
		Size: 20.9 MB (20946053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4ddd0a063cb5f89e516dc6684c1f37599b5f08cf8802b14c2619d667c428d0`  
		Last Modified: Tue, 17 Jan 2017 00:23:34 GMT  
		Size: 51.3 MB (51254010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824f7445bc49fbc5b85f9cb9f910c64e040cf8f251cd1e1d6b9406fa0c3bab8`  
		Last Modified: Fri, 10 Feb 2017 19:02:25 GMT  
		Size: 61.7 MB (61672725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349cce2345edc54630dcbd5928a66845c2941fd4e76665ae491452b0a2b95df4`  
		Last Modified: Fri, 10 Feb 2017 19:02:34 GMT  
		Size: 88.9 MB (88936123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa998d3aeb31907aba86ba5e6204694da632e473d1d6045a6c3980dd9149092f`  
		Last Modified: Fri, 10 Feb 2017 19:02:05 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cebfed37bef79d7baf732cf8b80fe1cefa29e5e1903e80172de588878f5d6ca`  
		Last Modified: Fri, 10 Feb 2017 19:02:05 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip