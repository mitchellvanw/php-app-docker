# PHP application starter with Docker

I was tired of having to copy these files around from project to project. So, here it is, a starter for your arbitrary php application.

## What does it dooooo?

Lots of stuff.

But, it includes:

* PHP (5 or 7, you choose)
* NGINX (also known as "engine x")
* MySQL 5.7 (pronounce it as "my ess cue ell")
* Redis 3.0 (just "redis")
* EventStore (talking about the geteventstore.com one)
* Memcached (are we caching memes now?)
* Beanstalkd (wait, do I have to climb that thing?)

There's more coming, like elasticsearch, and stuff.

## How does it work?

Well, first of all, magic. Secondly, it's the easiest thing you've ever done, after you installed the metric crap ton of required software.

I run OS X, which means I just installed Kitematic and it Just Works (tm).

For Linux, [click here](http://lmgtfy.com?q=install+docker+on+linux)

For Windows, [click here](http://lmgtfy.com?q=install+docker+on+windows)

Done? Great! Let's gooooo.

`$ docker-compose build & docker-compose up -d`

## It's not running, what did I do wrong?

Well, if you're like me, you've probably encountered every error humanly possible.
In this situation I advice you to [make an issue](https://github.com/mitchellvanw/php-app-docker/issues/new) or spend countless hours in StackOverflow.

## Image specific instructions
All images support environment variables using the following structure:
```
environment:
    - KEY=value
```
If you're a fan of passing in files then use the following structure:
```
env_file:
  - ./your-file.env
```

### EventStore
You can login using the docker and adding the port `2113`.
If the installation was successful you should be able to login using the following credentials:
- `admin`:`changeit`

## Internet Points

Docker is awesome, but [@nickstrnl](https://twitter.com/nickstrnl) is even more awesome. He did a lot of the work on this thing.
So, follow him on twitter, you won't regret it. Really, you won't, simply because he hardly ever tweets.

P.S. Nick,

Tweet more.
