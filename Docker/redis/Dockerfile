FROM redis:latest

VOLUME /data
WORKDIR /data

ADD redis.conf /usr/local/etc/redis/redis.conf

CMD ["redis-server"]
EXPOSE 6379