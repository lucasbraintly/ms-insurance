FROM nginx:1.17.6-alpine

MAINTAINER Braintly <info@braintly.com>

COPY ./default.conf /etc/nginx/conf.d/default.conf

# Install & clean up dependencies
RUN apk --no-cache --update --repository http://dl-3.alpinelinux.org/alpine/edge/community/ add \
    curl \
    shadow \
    inotify-tools \
    vim \   
&& apk --no-cache del \
    wget \
&& rm -rf /var/cache/apk/* /tmp/*


CMD ["nginx", "-g", "daemon off;"]