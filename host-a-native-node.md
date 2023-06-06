# Host a Native Node

After installation, you can create your configuration by:

```bash
rings init
```

This command will generate a configuration file named config.yaml for you. The default path is $HOME/.rings/config.yaml. You can also customize the path by using `rings init --location <path>`. Additionally, you can specify the key used by the Rings node by using `rings init -k <your private key>`.

By default, an ECDSA key pair will be automatically generated for you. The key pair in Rings Network is used for user identification and message signing. The key pair is utilized in various components of the network, so it is essential for users to ensure the security of their key pair. In the Native Node environment, since the private key is stored in plaintext, we strongly **discourage** the use of any asset-related key pair to host Rings Network.

Here is an example of how your config.yaml file might look:

<pre class="language-yaml"><code class="lang-yaml"><strong># cat ./config.yaml
</strong><strong>
</strong>bind: 127.0.0.1:50000
endpoint_url: http://127.0.0.1:50000
ecdsa_key: &#x3C;your private key>
ice_servers: stun://stun.l.google.com:19302
stabilize_timeout: 3
external_ip: null
backend: []
data_storage:
  path: /Users/foo/.rings/data
  capacity: 200000000
measure_storage:
  path: /Users/foo/.rings/measure
  capacity: 200000000
</code></pre>

We can see that there are several optional configurations available:

* `bind`: Interface for binding the Rings Network RPC service.
* `endpoint_url`: Interface for binding the Rings Network endpoint service, which supports creating WebRTC connection links via HTTP handshake.
* `ecdsa_key`: The key used for identity verification in Rings Network, generated based on the secp256k1 elliptic curve.
* `ice_servers`: STUN or TURN servers used for creating WebRTC connections. These servers are typically public services, such as the Google public STUN service. Multiple servers can be specified, for example:

```yaml
ice_servers: turn://ethereum.org:9090;stun://foo:bar@stun.l.google.com:19302
```

* `stabilize_timeout`: Timeout for each stabilization process in Rings Network, which helps maintain network stability.
* `external_id`: External IP address bound to Rings Network.
* `backend`: Rings Network can provide backend services, such as decentralizing a local service by forwarding information from Rings Network to it.
* `data_storage`: Rings Network is a DHT-based network, so it requires local data caching to ensure the smooth operation of lookup and other services. Users can specify the storage path and capacity (in bytes) for data storage.
* `measure_storage`: Rings Network uses a measure service to assess the network's robustness. It records scores given by nodes to neighboring nodes. Users can specify the storage path and capacity (in bytes) for measure data.



