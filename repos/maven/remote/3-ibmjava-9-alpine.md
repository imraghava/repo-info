## `maven:3-ibmjava-9-alpine`

```console
$ docker pull maven@sha256:df702a2e265d930bcece0558d566c439711de2480b9b65ffcb68045d481602e3
```

-	Platforms:
	-	linux; amd64

### `maven:3-ibmjava-9-alpine` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291578498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aedbed7cc2b5def0179d0eabcecbec3590cbb48eb3da0985d7f4e88a21b504`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:15:26 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 27 Jun 2017 20:22:22 GMT
RUN apk --update add --no-cache ca-certificates curl openssl xz     && GLIBC_VER="2.25-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && curl -Ls $ALPINE_GLIBC_REPO/$GLIBC_VER/glibc-$GLIBC_VER.apk > /tmp/$GLIBC_VER.apk     && apk add --allow-untrusted /tmp/$GLIBC_VER.apk     && curl -Ls https://www.archlinux.org/packages/core/x86_64/gcc-libs/download > /tmp/gcc-libs.tar.xz     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && apk del curl     && rm -rf /tmp/$GLIBC_VER.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/*
# Tue, 27 Jun 2017 20:22:24 GMT
ENV JAVA_VERSION=1.9.0_ea2
# Tue, 27 Jun 2017 20:23:41 GMT
RUN ESUM="0fe3712b54a93695cf4948d9ae171bf5cef038c0e41b364b4e9eb7cb80a60688"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="sdk/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Tue, 27 Jun 2017 20:52:36 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Jul 2017 17:14:51 GMT
RUN apk add --no-cache curl tar bash
# Mon, 10 Jul 2017 17:14:52 GMT
ARG MAVEN_VERSION=3.5.0
# Mon, 10 Jul 2017 17:14:52 GMT
ARG USER_HOME_DIR=/root
# Mon, 10 Jul 2017 17:14:53 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Mon, 10 Jul 2017 17:14:53 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Mon, 10 Jul 2017 17:14:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 10 Jul 2017 17:14:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 10 Jul 2017 17:14:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 10 Jul 2017 17:14:56 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 10 Jul 2017 17:14:57 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Mon, 10 Jul 2017 17:14:57 GMT
VOLUME [/root/.m2]
# Mon, 10 Jul 2017 17:14:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 10 Jul 2017 17:14:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edde235e180d278d0f6d8b128ef30bd565f323a84478e1938dc2eea3d48d2d8`  
		Last Modified: Tue, 27 Jun 2017 21:12:05 GMT  
		Size: 7.6 MB (7565466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2138b724adc562bba0fa93782e80e91f19740d616ed3a559b5f0f4a01a0bc037`  
		Last Modified: Tue, 27 Jun 2017 21:12:34 GMT  
		Size: 271.6 MB (271634815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67c3e2c85976e0df4b5ae2d278ded03c7d67c8348dcf68ac045bcfd2ccdb01`  
		Last Modified: Mon, 10 Jul 2017 17:21:52 GMT  
		Size: 1.7 MB (1713996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6087d690d5d71d4655fc56e26c30c42e3966c4a362d85fe5eb964cdfa9c5a3d`  
		Last Modified: Mon, 10 Jul 2017 17:21:53 GMT  
		Size: 8.7 MB (8672752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5137af33928a6cbbf6840bf6acab32f2ceb308115fcaa57246d100965d801b60`  
		Last Modified: Mon, 10 Jul 2017 17:21:52 GMT  
		Size: 719.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c848c0c3574ed7cdc5336d7f347194d13afab25c6e3b63b981b332bfd56f39`  
		Last Modified: Mon, 10 Jul 2017 17:21:52 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
