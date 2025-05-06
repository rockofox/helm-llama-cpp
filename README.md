# Llama.cpp Chart

Deploys [Llama.cpp server](https://github.com/ggerganov/llama.cpp/tree/master/examples/server) onto your Kubernetes
cluster, complete with a persistent volume to store the model files, replication, and an ingress. By default, uses
`lmstudio-ai/gemma-2b-it-GGUF` model, but this can be overridden with custom values.

## Installation

```shell
helm install llama-cpp https://rockofox.github.io/helm-llama-cpp/llama-cpp-0.0.5.tgz --namespace=llama-cpp
```

## Usage

By default, the ingress exposes the web UI at `llama.cluster.local`. Make sure to update your `/etc/hosts` file so the
new subdomain is accessible:

```
10.0.0.70 cluster.local llama.cluster.local
```
