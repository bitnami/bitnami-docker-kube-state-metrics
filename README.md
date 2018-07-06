[![CircleCI](https://circleci.com/gh/bitnami/bitnami-docker-kube-state-metrics/tree/master.svg?style=shield)](https://circleci.com/gh/bitnami/bitnami-docker-kube-state-metrics/tree/master)

# What is Kube-state-metrics?

kube-state-metrics is a simple service that listens to the Kubernetes API server and generates metrics about the state of the objects. (See examples in the Metrics section below.) It is not focused on the health of the individual Kubernetes components, but rather on the health of the various objects inside, such as deployments, nodes and pods.

The metrics are exported through the Prometheus golang client on the HTTP endpoint /metrics on the listening port (default 80). They are served either as plaintext or protobuf depending on the Accept header. They are designed to be consumed either by Prometheus itself or by a scraper that is compatible with scraping a Prometheus client endpoint. You can also open /metrics in a browser to see the raw metrics.

[https://github.com/kubernetes/kube-state-metrics](https://github.com/kubernetes/kube-state-metrics)

# TL;DR;

Deploy Kube-state-metrics on your [Kubernetes cluster](https://github.com/kubernetes/kube-state-metrics/tree/master/Documentation).

# Why use Bitnami Images?

* Bitnami closely tracks upstream source changes and promptly publishes new versions of this image using our automated systems.
* With Bitnami images the latest bug fixes and features are available as soon as possible.
* Bitnami containers, virtual machines and cloud images use the same components and configuration approach - making it easy to switch between formats based on your project needs.
* Bitnami images are built on CircleCI and automatically pushed to the Docker Hub.
* All our images are based on [minideb](https://github.com/bitnami/minideb) a minimalist Debian based container image which gives you a small base container image and the familiarity of a leading linux distribution.

# Supported tags and respective `Dockerfile` links

* [`1-ol-7`, `1.3.1-ol-7-r13` (1/ol-7/Dockerfile)](https://github.com/bitnami/bitnami-docker-kube-state-metrics/blob/1.3.1-ol-7-r13/1/ol-7/Dockerfile)
* [`1-debian-8`, `1.3.1-debian-8-r43`, `1`, `1.3.1`, `1.3.1-r43`, `latest` (1/Dockerfile)](https://github.com/bitnami/bitnami-docker-kube-state-metrics/blob/1.3.1-debian-8-r43/1/Dockerfile)
* [`1-debian-9`, `0.0.0-debian-9-r0` (1/debian-9/Dockerfile)](https://github.com/bitnami/bitnami-docker-kube-state-metrics/blob/0.0.0-debian-9-r0/1/debian-9/Dockerfile)

Subscribe to project updates by watching the [bitnami/kube-state-metrics GitHub repo](https://github.com/bitnami/bitnami-docker-kube-state-metrics).

# Get this image

The recommended way to get the Bitnami Kube-state-metrics Docker Image is to pull the prebuilt image from the [Docker Hub Registry](https://hub.docker.com/r/bitnami/kube-state-metrics).

```bash
$ docker pull bitnami/kube-state-metrics:latest
```

To use a specific version, you can pull a versioned tag. You can view the [list of available versions](https://hub.docker.com/r/bitnami/kube-state-metrics/tags/) in the Docker Hub Registry.

```bash
$ docker pull bitnami/kube-state-metrics:[TAG]
```

If you wish, you can also build the image yourself.

```bash
$ docker build -t bitnami/kube-state-metrics:latest https://github.com/bitnami/bitnami-docker-kube-state-metrics.git
```

# Configuration

## Resource recommendation

Resource usage changes with the size of the cluster. As a general rule, you should allocate

* 200MiB memory
* 0.1 cores

For clusters of more than 100 nodes, allocate at least

* 2MiB memory per node
* 0.001 cores per node

# Contributing

We'd love for you to contribute to this container. You can request new features by creating an [issue](https://github.com/bitnami/bitnami-docker-kube-state-metrics/issues), or submit a [pull request](https://github.com/bitnami/bitnami-docker-kube-state-metrics/pulls) with your contribution.

# Issues

If you encountered a problem running this container, you can file an [issue](https://github.com/bitnami/bitnami-docker-kube-state-metrics/issues). For us to provide better support, be sure to include the following information in your issue:

- Host OS and version
- Docker version (`docker version`)
- Output of `docker info`
- Version of this container
- The command you used to run the container, and any relevant output you saw (masking any sensitive information)

# License
Copyright 2018 Bitnami

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
