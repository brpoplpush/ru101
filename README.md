# RU101 — An Introduction to Redis Data Structures
<https://university.redislabs.com/courses/course-v1:redislabs+RU101+2019_03/course/>

Requirements:

* [Redis 5.x](https://docs.docker.com/samples/library/redis/)
* Python 3.6.5 (see [pyenv](https://github.com/pyenv/pyenv))

Setup:

* Make sure the following env variable are set: `REDIS_HOST`, `REDIS_PORT` and `PYTHONPATH`
* validate in the Terminal:

```
$ docker run --name redis-server \
  -p 127.0.0.1:6389:6379/tcp \
  -d redis:5-alpine redis-server \
  --appendonly yes
$ python helloworld.py
None
$ python utils/dumpload.py load ru101/data/ru101.json
total keys loaded: 14328
$ python helloworld.py
b'world'
$ redis-cli -p 6389
127.0.0.1:6389> dbsize
(integer) 14328
```

