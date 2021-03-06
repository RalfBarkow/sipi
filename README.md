[![Build Status](https://github.com/dasch-swiss/sipi/workflows/CI/badge.svg?branch=main)](https://github.com/dasch-swiss/sipi/actions)

# Overview

Sipi is a high-performance media server developed by the [Digital Humanities Lab](http://www.dhlab.unibas.ch) at the
[University of Basel](https://www.unibas.ch/en.html). It is designed to be used by archives,
libraries, and other institutions that need to preserve high-quality images
while making them available online.

Sipi implements the [International Image Interoperability Framework (IIIF)](http://iiif.io/),
and efficiently converts between image formats, preserving metadata contained
in image files. In particular, if images are stored in [JPEG 2000](https://jpeg.org/jpeg2000/) format,
Sipi can convert them on the fly to formats that are commonly used on the
Internet. Sipi offers a flexible framework for specifying authentication and
authorization logic in [Lua](https://www.lua.org/) scripts, and supports restricted access to images,
either by reducing image dimensions or by adding watermarks. It can easily be
integrated with [Knora](http://www.knora.org).

Sipi is [free software](http://www.gnu.org/philosophy/free-sw.en.html),
released under the [GNU Affero General Public License](http://www.gnu.org/licenses/agpl-3.0.en.html).

It is written in C++ and runs on Linux (including Debian, Ubuntu, and CentOS) and
Mac OS X.

Freely distributable binary releases will be available soon.

# Documentation

The documentation is online at https://sipi.io.

To build it locally, you will need [MkDocs](https://www.mkdocs.org/).
In the root the source tree, type:

```
make docs-build
```

You will then find the manual under `site/index.html`.

# Building from source

All should be run from inside the root of the repository.

## Build and run inside Docker - recommended
```bash
$ make compile
$ make test
$ make run
```

## Build under macOS - not recommended. You are on your own. We warned you ;-)

```bash
$ (mkdir -p ./build-mac && cd build-mac && cmake .. && make && ctest --verbose)
```

# Releases

Releases are published on Dockerhub: https://hub.docker.com/repository/docker/daschswiss/sipi


# Contact Information

Lukas Rosenthaler `<lukas.rosenthaler@unibas.ch>`
