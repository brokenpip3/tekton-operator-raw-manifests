# Tekton operator raw manifests

## Why?

If you need to install tekton operator https://github.com/tektoncd/operator with
a gitops like mechanism (ex: Flux) there is no official helm chart or valid raw
k8s manifests.

This repo contains a ci flow that produce, update and tag any new tekton
operator version in raw k8s yaml files.

## How it works?

* Check if new operator version is present
* Download the official manifest and split them by kind and name
* Commit the changes and tag a new release in this repo

See [new-release](./hack/new-release.sh)

