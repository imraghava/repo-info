## `groovy:jdk7`

```console
$ docker pull groovy@sha256:108f3f94c5404f0f29bcfe8be240e9796593989e0dbd502be7e63c2eb4d6380f
```

-	Platforms:
	-	linux; amd64

### `groovy:jdk7` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339124678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7767ed1cbc7c732c4bdbb1c209f34dfcb4f7dfceec35f183adb8269ec40143e`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 21:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Jun 2017 21:06:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jun 2017 01:52:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jun 2017 01:52:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jun 2017 01:52:16 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 23 Jun 2017 01:52:17 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 23 Jun 2017 01:52:18 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 23 Jun 2017 01:52:19 GMT
ENV JAVA_VERSION=7u131
# Fri, 23 Jun 2017 01:52:20 GMT
ENV JAVA_DEBIAN_VERSION=7u131-2.6.9-2~deb8u1
# Fri, 23 Jun 2017 01:56:03 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 23 Jun 2017 14:58:17 GMT
CMD ["groovysh"]
# Fri, 23 Jun 2017 14:58:18 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 27 Jun 2017 18:11:14 GMT
ENV GROOVY_VERSION=2.4.12
# Tue, 27 Jun 2017 18:11:44 GMT
RUN set -o errexit -o nounset 	&& echo "Downloading Groovy" 	&& wget --no-verbose --output-document=groovy.zip "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip" 		&& echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server" 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in 		"7FAA0F2206DE228F0DB01AD741321490758AAD6F" 		"331224E1D7BE883D16E8A685825C06C827AF6B66" 		"34441E504A937F43EB0DAEF96A65176A0FB1CD0B" 		"9A810E3B766E089FFB27C70F11B595CEDC4AEBB5" 	; do 		for server in 			ha.pool.sks-keyservers.net 			hkp://p80.pool.sks-keyservers.net:80 			pgp.mit.edu 		; do 			echo "  Trying ${server}"; 			if gpg --keyserver "${server}" --recv-keys "${key}"; then 				break; 			fi; 		done; 	done; 	if [ $(gpg --list-keys | grep -c "pub ") -ne 4 ]; then 		echo "ERROR: Failed to fetch GPG keys" >&2; 		exit 1; 	fi 		&& echo "Checking download signature" 	&& wget --no-verbose --output-document=groovy.zip.asc "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc" 	&& gpg --batch --verify groovy.zip.asc groovy.zip 	&& rm --recursive "${GNUPGHOME}" 	&& rm groovy.zip.asc 		&& echo "Installing Groovy" 	&& unzip groovy.zip 	&& rm groovy.zip 	&& mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/" 	&& ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape 	&& ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy 	&& ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc 	&& ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole 	&& ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc 	&& ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh 	&& ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy 		&& echo "Adding groovy user and group" 	&& groupadd --system --gid 1000 groovy 	&& useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy 	&& mkdir --parents /home/groovy/.groovy/grapes 	&& chown --recursive groovy:groovy /home/groovy
# Tue, 27 Jun 2017 18:12:29 GMT
USER [groovy]
# Tue, 27 Jun 2017 18:12:54 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 27 Jun 2017 18:13:19 GMT
WORKDIR /home/groovy
# Tue, 27 Jun 2017 18:13:48 GMT
RUN set -o errexit -o nounset 	&& echo "Testing Groovy installation" 	&& groovy --version
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3942a742d221ef22a0a335c4eebf09e15a36dcfb224b5a2d0cdcc405f374ccb`  
		Last Modified: Wed, 21 Jun 2017 00:33:28 GMT  
		Size: 19.3 MB (19264368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b1123c88f67a9ad43d9bf3f552bbe3352696a674e82712fda785db4f71a655`  
		Last Modified: Wed, 21 Jun 2017 00:34:52 GMT  
		Size: 43.2 MB (43227273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd20aef2091895544e1f428c076d83267e49462e9c8ce7b19516940fa360f818`  
		Last Modified: Fri, 23 Jun 2017 14:09:03 GMT  
		Size: 594.4 KB (594399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3895ad605979a7a7252d1963cab8ac214d7c44be04da35ab0447c4e965fd8ad`  
		Last Modified: Sat, 24 Jun 2017 16:54:51 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37ee48745eb89786a1c1041a9959c3b3cde92677a5999448f537185d29d55cf`  
		Last Modified: Sat, 24 Jun 2017 16:54:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67cb815527964e50938dd1690f5d9d617edba7a6b083e6b6f41506584ccb9fe`  
		Last Modified: Sat, 24 Jun 2017 16:56:28 GMT  
		Size: 187.0 MB (186961492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58a80befca9ff8d16c46cb1ff620104d372dbc297e13f1d8bd876f87a766f53`  
		Last Modified: Tue, 27 Jun 2017 18:36:27 GMT  
		Size: 36.5 MB (36461827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ed6f76890767ae42e480a63c22d166e72c82c400152b5d72230a57ba2dd96`  
		Last Modified: Tue, 27 Jun 2017 18:36:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
