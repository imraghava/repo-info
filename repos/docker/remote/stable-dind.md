## `docker:stable-dind`

```console
$ docker pull docker@sha256:fbd827a4cd92b82822ffbc4cd453f25ce3c5f7e260b4a6ca9838f4c159f31a7d
```

-	Platforms:
	-	linux; amd64

### `docker:stable-dind` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32775218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f40a275afb001ef3646d435713072b80d0755c482d1594202d19ca069d35fa2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 27 Jun 2017 18:39:21 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Tue, 27 Jun 2017 18:39:45 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:09:43 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 27 Jun 2017 20:15:25 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 29 Jun 2017 21:39:59 GMT
ENV DOCKER_VERSION=17.03.2-ce
# Thu, 29 Jun 2017 21:40:06 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Thu, 29 Jun 2017 21:40:08 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Thu, 29 Jun 2017 21:40:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jun 2017 21:40:34 GMT
CMD ["sh"]
# Thu, 29 Jun 2017 21:41:29 GMT
RUN apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz
# Thu, 29 Jun 2017 21:41:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 29 Jun 2017 21:41:55 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Thu, 29 Jun 2017 21:42:00 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Thu, 29 Jun 2017 21:42:01 GMT
COPY file:7070e4b35c137a8ec5904300d19b8f7ee74aa76659517767c617249cece98a4a in /usr/local/bin/ 
# Thu, 29 Jun 2017 21:42:02 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Jun 2017 21:42:03 GMT
EXPOSE 2375/tcp
# Thu, 29 Jun 2017 21:42:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Jun 2017 21:42:05 GMT
CMD []
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9253de26747cb9ad807096c7779b82609261ad1c5cbee1e502a86c9b0af4da`  
		Last Modified: Thu, 29 Jun 2017 19:08:48 GMT  
		Size: 350.6 KB (350624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d097821ea2c9d225166fe3401d4fb3539096cd03f47ecf2605fcb5c6583a9e92`  
		Last Modified: Thu, 29 Jun 2017 22:13:16 GMT  
		Size: 28.1 MB (28110648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f5b9db32b4c9eec4278d5c656bf09154420adf7a44292a765d216de6df08eb`  
		Last Modified: Thu, 29 Jun 2017 22:13:08 GMT  
		Size: 729.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cc7e160b045bbb58540ce72961e74300ee2eb3d473d7ea084e8222b0dc6596`  
		Last Modified: Thu, 29 Jun 2017 22:16:56 GMT  
		Size: 2.2 MB (2165476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c403799a483c389cbb30e75a706c4f9c99dab8f4c4d041546818b5272e80a67f`  
		Last Modified: Thu, 29 Jun 2017 22:16:54 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d0c64cd1ec3fe5373f6f5b23ab3a6b38311d4e208ee29ec8e84cf73fe3c99b`  
		Last Modified: Thu, 29 Jun 2017 22:16:54 GMT  
		Size: 175.7 KB (175679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d148546f89ae558faac06fa61e5ad399573e94caa4dddee874e3a7c7a0091d1`  
		Last Modified: Thu, 29 Jun 2017 22:16:58 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
