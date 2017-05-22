############################################################ 
# Dockerfile to build image php
# Based on Debian:jessie(8)
############################################################

FROM library/php:7.1-fpm
MAINTAINER XinYe <nunchuk@live.com>

# add AliCloud repository
# > If you are using Aliyun ECS, the package mirror server can be replaced by 
# > 'mirrors.cloud.aliyuncs.com', via Aliyun private network.
RUN { \
		echo 'deb http://mirrors.aliyun.com/debian/ jessie main non-free contrib'; \
	    echo 'deb http://mirrors.aliyun.com/debian/ jessie-proposed-updates main non-free contrib'; \
	    echo 'deb-src http://mirrors.aliyun.com/debian/ jessie main non-free contrib'; \
	    echo 'deb-src http://mirrors.aliyun.com/debian/ jessie-proposed-updates main non-free contrib'; \
  	} > /etc/apt/sources.list

ENV TIMEZONE=Asia/Shanghai

# set timezone
RUN rm /etc/localtime && ln -sf /usr/share/zoneinfo/${TIMEZONE} /etc/localtime