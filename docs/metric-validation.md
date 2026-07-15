Identify a Longhorn Manager pod:

kubectl -n longhorn-system get pods \
  -l app=longhorn-manager

Forward the metrics endpoint:

kubectl -n longhorn-system port-forward \
  pod/<LONGHORN_MANAGER_POD> 9500:9500

Check the required metrics:

curl -s http://127.0.0.1:9500/metrics |
  grep -E '^longhorn_(volume|node|disk|replica|engine|manager)_'

Validate individual metrics:

curl -s http://127.0.0.1:9500/metrics |
  grep '^longhorn_volume_robustness'
curl -s http://127.0.0.1:9500/metrics |
  grep '^longhorn_node_status'
curl -s http://127.0.0.1:9500/metrics |
  grep '^longhorn_disk_'
curl -s http://127.0.0.1:9500/metrics |
  grep -E '^longhorn_(replica_state|engine_state|engine_replica_mode)'
