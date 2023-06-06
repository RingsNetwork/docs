# Hidden services

Rings Network enables users to integrate services into its decentralized network. Its underlying mechanism relies on Rings DHT for service registration and discovery. Setting up hidden services is a straightforward process that decentralizes any service with just a few simple steps.

## Config your backend

Rings allows users to configure hidden services through the "config.yaml" file. If you are not familiar with what "config.yaml" is, I recommend reading up on it.

[config.yaml.md](../advanced-topic/config.yaml.md "mention")

For a hidden service, three fields need to be provided: "name," "register\_service," and "prefix". For example:

```yaml
- name: ipfs
  register_service: ipfs_provider
  prefix: http://127.0.0.1:8080
```

This config will perform two tasks:

1. It will use the "register\_service" function to register itself as an "ipfs\_provider" within the Rings Network.
2. It will forward all incoming traffic from the Rings Network to the specified "prefix."

Now let's integrate it into the `config.yaml` file:

```bash
# cat ./config.yaml

bind: 127.0.0.1:50000
endpoint_url: http://127.0.0.1:50000
ecdsa_key: <your private key>
ice_servers: stun://stun.l.google.com:19302
stabilize_timeout: 3
external_ip: null
backend:
- name: ipfs
  register_service: ipfs_provider
  prefix: http://127.0.0.1:8080
...
```





###

