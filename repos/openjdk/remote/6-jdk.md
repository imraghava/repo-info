## `openjdk:6-jdk`

```console
$ docker pull openjdk@sha256:1112c1cfb80e5bfa9bf9a9316b578ba469ae1ba11ebcf0c7082e8f1cd8574f87
```

-	Platforms:
	-	linux; amd64

### `openjdk:6-jdk` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189506238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f88b2f43b2e36e4aca466518445662e0b151ac63a746fef8208613c71c2b28`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 Jun 2017 20:29:57 GMT
ADD file:e58836121f9e162887b70de3a328bb9ff8944a1307cf5f05b9d768a1a49afe60 in / 
# Tue, 20 Jun 2017 20:29:58 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 23:05:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jul 2017 02:16:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jul 2017 02:17:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jul 2017 03:51:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jul 2017 03:52:03 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jul 2017 03:52:05 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 07 Jul 2017 03:52:07 GMT
RUN ln -svT "/usr/lib/jvm/java-6-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 07 Jul 2017 03:52:34 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 07 Jul 2017 03:52:35 GMT
ENV JAVA_VERSION=6b38
# Fri, 07 Jul 2017 03:52:36 GMT
ENV JAVA_DEBIAN_VERSION=6b38-1.13.10-1~deb7u1
# Fri, 07 Jul 2017 03:53:09 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		openjdk-6-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:5b825a4651ef2855128f8b498adaf68d54840a4b4b66c406e4ea30ede531f1fd`  
		Last Modified: Tue, 20 Jun 2017 21:02:17 GMT  
		Size: 38.1 MB (38103640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0be653e0fcc6c891b4087051f57520a0842eb3dc1851303e3033a19b826c96`  
		Last Modified: Wed, 21 Jun 2017 01:04:25 GMT  
		Size: 6.9 MB (6948769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b8077f63a8fc0b4991f6c698d4b5d97b6148a25a0f61136daffb5333f87f7`  
		Last Modified: Fri, 07 Jul 2017 03:28:12 GMT  
		Size: 37.9 MB (37938306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51887ad4dc9991dbcd1b330b8445e239ecb9b949e9d5f84cf66108ae3009aea`  
		Last Modified: Fri, 07 Jul 2017 05:56:31 GMT  
		Size: 414.4 KB (414416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6d10c983b4ddc1c2af2ca81f8d9925519a2d60590fdb1fe7a50ad87d11668e`  
		Last Modified: Fri, 07 Jul 2017 05:56:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8296a8e28df5f80eb24a058623de4adae337863accd9a7c1ebdf14ee0b21a461`  
		Last Modified: Fri, 07 Jul 2017 05:56:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19caf90207560047721692f7642bd30bd8f16bf3dc3e954deb3be280d2b68bae`  
		Last Modified: Fri, 07 Jul 2017 05:56:50 GMT  
		Size: 106.1 MB (106100737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
