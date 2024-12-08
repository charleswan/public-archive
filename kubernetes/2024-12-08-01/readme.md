Originally From [here](https://raw.githubusercontent.com/techiescamp/kubeadm-scripts/main/manifests/metrics-server.yaml).

Context:

To install the metrics server, execute the following metric server manifest file. It deploys metrics server version `v0.7.1`

```sh
kubectl apply -f https://raw.githubusercontent.com/techiescamp/kubeadm-scripts/main/manifests/metrics-server.yaml
```

This manifest is taken from the official [metrics server](https://github.com/kubernetes-sigs/metrics-server) repo. I have added the `--kubelet-insecure-tls` flag to the container to make it work in the local setup and hosted it separately. Or else, you will get the following error.

```sh
 because it doesn't contain any IP SANs" node=""
```

Reference:

- [How To Setup Kubernetes Cluster Using Kubeadm](https://devopscube.com/setup-kubernetes-cluster-kubeadm/)
