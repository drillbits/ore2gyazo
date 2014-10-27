# Create Data-only Container

```
$ docker build -t drillbits/gyazo-storage storage
$ docker run -d -i --name gyazo_storage drillbits/gyazo-storage
```

# Run server

## Create server container

```
$ docker build -t drillbits/gyazo-server server
$ docker run -d -i -p 80 --volumes-from gyazo_storage drillbits/gyazo-server
```
