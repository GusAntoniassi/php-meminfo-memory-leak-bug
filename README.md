# php-meminfo-memory-leak-bug
This container was made to reproduce the bug reported in issue #81 at php-meminfo

https://github.com/BitOne/php-meminfo/issues/81

How to reproduce the bug:

```bash
docker pull gusantoniassi/php-meminfo-memory-leak-bug
docker run -it --rm gusantoniassi/php-meminfo-memory-leak-bug bash
cd /opt/php-meminfo/extension/php7
make test

# test dump-memory_leak.phpt should fail
```
