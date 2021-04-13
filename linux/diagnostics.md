# To see how hardware is connected inside

```bash
numactl -H

nvidia-smi topo -m
```

# Packages conflicts list

```bash
apt-cache show libcurl4-openssl-dev | grep Conflicts
Conflicts: libcurl4-gnutls-dev, libcurl4-nss-dev, libssl-dev (<< 1.1), libssl1.0-dev
Conflicts: libcurl4-gnutls-dev, libcurl4-nss-dev, libssl-dev (<< 1.1), libssl1.0-dev
```
