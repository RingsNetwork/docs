# Exchange SDP

We will explain how the handshake works by establishing a connection between two nodes manually. Let's start two nodes using config1.yaml and config2.yaml, which will make the nodes listen on ports 50000 and 50001 respectively.

```yaml
# config1.yaml

bind: 127.0.0.1:50000
endpoint_url: http://127.0.0.1:50000
ecdsa_key: <privite key>
ice_servers: stun://stun.l.google.com:19302
stabilize_timeout: 3
external_ip: null
backend: []
data_storage:
  path: /Users/foo/.rings/data2
  capacity: 200000000
measure_storage:
  path: /Users/foo/.rings/measure2
  capacity: 200000000

```

```yaml
# config2.yaml

bind: 127.0.0.1:50001
endpoint_url: http://127.0.0.1:50001
ecdsa_key: <private key>
ice_servers: stun://stun.l.google.com:19302
stabilize_timeout: 3
external_ip: null
backend: []
data_storage:
  path: /Users/ryan/.rings/data1
  capacity: 200000000
measure_storage:
  path: /Users/ryan/.rings/measure1
  capacity: 200000000

```

### # Run !

We launch two nodes with command:

```bash
cargo run -- run -c config1.yaml
cargo run -- run -c config2.yaml
```

