kubectl -n longhorn-system port-forward pod/<manager> 9500:9500

curl localhost:9500/metrics | grep longhorn
