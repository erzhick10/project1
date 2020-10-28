FROM ubuntu:16.04
ENV version 4.6.2
ADD https://s3-us-west-2.amazonaws.com/grafana-releases/release/grafana-$version.linux-x64.tar.gz /grafana/
WORKDIR /grafana
WORKDIR /grafana/grafana-$version

RUN tar -zxvf grafana-$version.linux-x64.tar.gz -C ./ && \

rm grafana-$version.linux-x64.tar.gz && \

ln -s /grafana/grafana-$version/bin/grafana-server /usr/bin/

COPY conf .
CMD ["/usr/bin/grafana-server"]
docker build -t grafana .

#FROM ubuntu

#RUN apk add --no-cache curl wget busybox-extras netcat-openbsd python py-pip && \
#    pip install awscli
#RUN apk --purge -v del py-pip
#CMD tail -f /dev/null
