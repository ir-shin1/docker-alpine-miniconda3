[![Docker Stars](https://img.shields.io/docker/stars/frolvlad/alpine-miniconda3.svg?style=flat-square)](https://hub.docker.com/r/frolvlad/alpine-miniconda3/)
[![Docker Pulls](https://img.shields.io/docker/pulls/frolvlad/alpine-miniconda3.svg?style=flat-square)](https://hub.docker.com/r/frolvlad/alpine-miniconda3/)


Miniconda Python 3.8 Docker image
=================================

This image is based on Alpine Linux image, which is only a 5MB image, and contains
[Python 3.8](https://www.python.org/) packaged by Continuum with Conda package manager.

Download size of this image is only:

[![](https://images.microbadger.com/badges/image/frolvlad/alpine-miniconda3.svg)](http://microbadger.com/images/frolvlad/alpine-miniconda3 "Get your own image badge on microbadger.com")

NOTE: Conda repositories contain only Glibc linked packaged binaries for Linux,
so we have to use
[glibc workaround](https://github.com/gliderlabs/docker-alpine/issues/11) on
Alpine.


Usage Example
-------------

```bash
$ docker run --rm miniconda3:py38_4.8.2 python -c 'print("Hello World")'
```

```bash
docker run -i -t -p 8888:8888 miniconda3:py38_4.8.2 /bin/sh -c "/opt/conda/bin/conda install jupyter -y --quiet && mkdir /opt/notebooks && /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --allow-root --no-browser"
```

Once you have run this command you will get printed 'Hello World' from Python!

NOTE: `conda` and `pip` are also available in this image.
