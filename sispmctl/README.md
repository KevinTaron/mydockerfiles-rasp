# Docker Build Command
```
docker build -t kevintaron/sispmctl-arm:latest .
```

# Run the Image:

```
docker run -t -i --privileged -v /dev/bus/usb:/dev/bus/usb kevintaron/sispmctl-arm:latest
```

# Rename & Start Container
```
docker rename xxx sisp
docker start sisp
```

# Use sispmctl
```
docker exec sisp sispmctl -o 1
docker exec sisp sispmctl -f 1
```
