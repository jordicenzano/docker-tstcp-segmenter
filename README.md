# docker-tstcp-segmenter
Docker image definition with an TS TCP to HLS segmenter tool installed (Segmenter's source code: [online-segmenter](https://jordicenzano.github.io/transport-stream-online-segmenter/))

# Pulling docker image from docker hub
1. Ensure you have [docker](https://www.docker.com) installed
2. Type: `docker pull jcenzano/tstcp-segmenter`

# Creating the docker image locally (optional)
1. Ensure you have docker [docker](https://www.docker.com) and make installed
2. Type `make`

# Testing the image
1. You can test the image with this command (you should see the tool's help):
```
docker run --rm -it jcenzano/tstcp-segmenter
```

# Using the image
You can call TS TCP segmenter docker like you call the local command, just adding the TS TCP segmenter parameters (*) at the end of the docker run call, synchronous example:
```
docker run --rm -it jcenzano/tstcp-segmenter 5000 /tmp media_ out.m3u8 4 127.0.0.1 event
```
You can also running it in background (daemon) with `-d`:
```
docker run --rm -itd jcenzano/tstcp-segmenter 5000 /tmp media_ out.m3u8 4 127.0.0.1 event
```

(*) See [online-segmenter](https://jordicenzano.github.io/transport-stream-online-segmenter/) for more information about possible parameters.