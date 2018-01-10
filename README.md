## To run the node

1) Install Nvidia Docker

https://github.com/NVIDIA/nvidia-docker

2) Run the node

```
docker run --runtime=nvidia -it -p 7075:7075/udp -p 7075:7075 -p 127.0.0.1:7076:7076 -v PATH_TO_LOCAL_DATA_DIRECTORY:/root/data chriscohoat/raiblocks-node-gpu
```

## General Diagnostics

```
docker run --runtime=nvidia -it chriscohoat/raiblocks-node-gpu ./rai_node --diagnostics
```

## OpenCL Diagnostics

```
docker run --runtime=nvidia -it chriscohoat/raiblocks-node-gpu ./rai_node --debug_opencl --platform=0 --device=0 --threads=1048576
```

## To build this repo

```
docker build -t chriscohoat/raiblocks-node-gpu .
```
