## `docker:test-git`

```console
$ docker pull docker@sha256:ad3d0f1fbaa58c0efb851a2eeff147f460dad3a11d59a899cbee3745c9a7bb6f
```

-	Platforms:
	-	linux; amd64

### `docker:test-git` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44064259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f503249e97275c39acdfa7a297ef9e1b3eaed057b3b8ea197eb58eddf9772e0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:22:16 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 27 Jun 2017 20:22:17 GMT
ENV DOCKER_CHANNEL=test
# Fri, 14 Jul 2017 21:59:19 GMT
ENV DOCKER_VERSION=17.06.1-ce-rc1
# Fri, 14 Jul 2017 21:59:26 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Fri, 14 Jul 2017 21:59:27 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Fri, 14 Jul 2017 21:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2017 21:59:28 GMT
CMD ["sh"]
# Fri, 14 Jul 2017 22:00:01 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf6059e353ab57887578aa1be4a24bdd7519f63dde8d79b973d67164f3e349`  
		Last Modified: Thu, 29 Jun 2017 19:32:29 GMT  
		Size: 351.3 KB (351302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df96975acc07347c62579f52c51e8c48c3af53508a140d7a5bd3b393bb6c77c`  
		Last Modified: Fri, 14 Jul 2017 22:00:24 GMT  
		Size: 30.0 MB (29989141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d50017aa3f2a4d0402a5bb7800b75527d1c931ddaa6405214e50047d4c4598`  
		Last Modified: Fri, 14 Jul 2017 22:00:18 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57647886b44775b9d4028425207cfab5399e75d628cb0553d7015fef7fbb60bb`  
		Last Modified: Fri, 14 Jul 2017 22:02:28 GMT  
		Size: 11.7 MB (11732688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
