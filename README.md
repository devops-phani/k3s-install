# k3s-install

Install k3s specific version and disable traefik

Ref

- https://github.com/k3s-io/k3s/releases/
- https://docs.k3s.io/installation/configuration

```
curl -sfL https://get.k3s.io | K3S_KUBECONFIG_MODE="644" INSTALL_K3S_VERSION="v1.23.15+k3s1" INSTALL_K3S_EXEC="--disable=traefik" sh -
```

Add additional IP's for generate the ssl

```
curl -sfL https://get.k3s.io | K3S_KUBECONFIG_MODE="644" INSTALL_K3S_VERSION="v1.23.15+k3s1" INSTALL_K3S_EXEC="--disable=traefik --tls-san 192.168.3.10" sh -
```
