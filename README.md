eatmemory
=========

## 1. Introduction
Simple utility to allocate memory on a computer

## 2. What can I use this for?
- Test swap
- Test behaviors on a machine when there is little memory available

## 3. Usage

### Installation

```
cd /tmp
git clone https://github.com/julman99/eatmemory.git
cd eatmemory
sudo make install
```

### Running

```
eatmemory <size>
```

Size is in number of bytes, megabytes or gigabytes.

### Examples

```
eatmemory 1024
eatmemory 10M
eatmemory 4G
```

## 4. Docker image

Example how to run a container which eats 128MB:

```
$ docker run -d --name mycontainer zoobab/eatmemory:latest 128MB
```

Check the memory consumption of the container:

```
$ docker stats --no-stream=true mycontainer
CONTAINER           CPU %               MEM USAGE / LIMIT       MEM %               NET I/O             BLOCK I/O             PIDS
mycontainer         0.00%               133.9 MiB / 3.651 GiB   3.58%               2.01 kB / 1.08 kB   1.217 MB / 3.265 MB   4
```
