FROM redis:3.0

VOLUME /data
WORKDIR /data

ADD redis.conf /usr/local/etc/redis/redis.conf

CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]
EXPOSE 6379