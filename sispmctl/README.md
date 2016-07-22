# Docker Build Command
```
docker build -t sispmctl:latest .
```

# Run the Image:

```
docker run -t -i --privileged -v /dev/bus/usb:/dev/bus/usb sispmctl:latest
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