# CircleI Docker Images

## Why

Docker provides official images for popular languages and services that are aimed to work in common context, whether in development or in production. CircleCI highly recommends using them for creating custom images that are more appropriate for users.

However, we frequently found them lacking some tools making them appropriate for dev/CI use. CircleCI publishes this image to extend the images in the following ways:

Common tools used in development and CI are installed e.g. `git`, `ssh`, `tar`, `ca-certificates`, `curl`, `wget`.
Docker tools: latest `docker`, `docker-compose`, and `dockerize` are installed


## Packages Included

- node 8.12
- docker
- docker-compose
- git
- make
- curl
- awscli
- awsebcli
- bash

## Usage

In the `.circleci/config.yml` file at the root of your project, you should add:

```yaml
...
  docker:
    - image: xogroup/docker-git-make-eb:1.0.1
...

```

The first image listed in the file defines the primary container image where all steps will run.

## Release

Once you commit and push the changes to `github.com/xogroup` organization, Dockerhub will pull the changes and build the image automatically.
