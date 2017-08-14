** redis

redis 安装 采用 https://hub.docker.com/_/redis/

** flower

celery -A tasks worker --loglevel=info

Open another shell and run flower:

celery -A tasks flower --loglevel=info

```
In [1]: from tasks import add

In [2]: result=add.delay(4, 4)

In [3]: result.ready()
Out[3]: False

In [4]: result.ready()
Out[4]: False
```
