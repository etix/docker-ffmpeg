# docker-ffmpeg
An FFmpeg Dockerfile built from source. Built on Alpine Linux.

* ffmpeg 4.3.1 (compiled from source)

[![Docker Stars](https://img.shields.io/docker/stars/alfg/ffmpeg.svg)](https://hub.docker.com/r/alfg/ffmpeg/)
[![Docker Pulls](https://img.shields.io/docker/pulls/alfg/ffmpeg.svg)](https://hub.docker.com/r/alfg/ffmpeg/)
[![Docker Automated build](https://img.shields.io/docker/automated/alfg/ffmpeg.svg)](https://hub.docker.com/r/alfg/ffmpeg/builds/)
[![Build Status](https://travis-ci.org/alfg/docker-ffmpeg.svg?branch=master)](https://travis-ci.org/alfg/docker-ffmpeg)

## Usage

* Pull Docker image and run:
```
docker pull alfg/ffmpeg
docker run -it --rm alfg/ffmpeg ffmpeg -buildconf
```

* or build and run container from source:

```
docker build -t ffmpeg .
docker run -it ffmpeg ffmpeg -buildconf
```

* or use as a base image in your Dockerfile:
```
FROM alfg/ffmpeg:latest
```

## FFmpeg Snapshot Builds
For building ffmpeg from snapshot, see [snapshot/Dockerfile](/snapshot/Dockerfile) for FFmpeg snapshot builds including support for AV1 (libaom).

Or pull from the Docker tag:
```
docker pull alfg/ffmpeg:snapshot
```

### FFmpeg Build
```
ffmpeg version 4.3.1 Copyright (c) 2000-2020 the FFmpeg developers
  built with gcc 9.3.0 (Alpine 9.3.0)
  configuration: --enable-version3 --enable-gpl --enable-nonfree --enable-small --enable-libmp3lame --enable-libx264 --enable-libx265 --enable-libvpx --enable-libtheora --enable-libvorbis --enable-libopus --enable-libfdk-aac --enable-libass --enable-libwebp --enable-librtmp --enable-postproc --enable-avresample --enable-libfreetype --enable-openssl --disable-debug --disable-doc --disable-ffplay --extra-cflags=-I/opt/ffmpeg/include --extra-ldflags=-L/opt/ffmpeg/lib --extra-libs='-lpthread -lm' --prefix=/opt/ffmpeg
  libavutil      56. 51.100 / 56. 51.100
  libavcodec     58. 91.100 / 58. 91.100
  libavformat    58. 45.100 / 58. 45.100
  libavdevice    58. 10.100 / 58. 10.100
  libavfilter     7. 85.100 /  7. 85.100
  libavresample   4.  0.  0 /  4.  0.  0
  libswscale      5.  7.100 /  5.  7.100
  libswresample   3.  7.100 /  3.  7.100
  libpostproc    55.  7.100 / 55.  7.100
  configuration:
    --enable-version3
    --enable-gpl
    --enable-nonfree
    --enable-small
    --enable-libmp3lame
    --enable-libx264
    --enable-libx265
    --enable-libvpx
    --enable-libtheora
    --enable-libvorbis
    --enable-libopus
    --enable-libfdk-aac
    --enable-libass
    --enable-libwebp
    --enable-librtmp
    --enable-postproc
    --enable-avresample
    --enable-libfreetype
    --enable-openssl
    --disable-debug
    --disable-doc
    --disable-ffplay
    --extra-cflags=-I/opt/ffmpeg/include
    --extra-ldflags=-L/opt/ffmpeg/lib
    --extra-libs='-lpthread -lm'
    --prefix=/opt/ffmpeg
```

## Resources
* https://alpinelinux.org/
* https://www.ffmpeg.org

## License
MIT
