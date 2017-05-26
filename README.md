## fluent-cat-container

A sandbox for testing fluentd settings.

### requirements

* Docker(moby)

### start fluentd

```sh
./fluentd
```

### fluent-cat

```sh
echo '{ "foo": "bar" }' | ./fluent-cat debug.log
```

### tail

`./log` is mounted on `/var/log` in the container.

```sh
cat sample.log > log/sample.log
```

### settings

Fix `tag` in `fluentd` file.

```
# default is v0.12.36
tag=v0.12.36
```

https://github.com/fluent/fluentd-docker-image
