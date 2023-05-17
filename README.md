# Introduction

<figure><img src="https://camo.githubusercontent.com/1e8e8235037707bbdc8e2a24242e5874b8be89b971f0ae552585b46398971b6f/68747470733a2f2f7374617469632e72696e67736e6574776f726b2e696f2f72696e67736e6574776f726b5f6c6f676f2e706e67" alt=""><figcaption></figcaption></figure>

Rings Network is a purely peer-to-peer network implementation. We use WebRTC to establish peer connections, and use WebAssembly to allow nodes to run in the browser. Rings Network uses the DHT (Chord) algorithm for message routing/addressing.

By introducing decentralized PKI (public key infrastructure) such as Ethereum and Bitcoin, we have built a series of cryptographic-based network infrastructures. For example, we support end-to-end and hop-by-hop encryption systems, service discovery and registration systems based on resource hashes, and so on.

## # Beginning



## # Principle







Rings Network is A peer-to-peer (P2P) network layer implementation based on the Chord algorithm. It does not have a consensus layer and is very lightweight, yet it can support up to 2^160 nodes online.

Additionally, due to its support for webassembly, Rings Node can easily run in a browser environment. The core concept of Rings Network is to divide the entire P2P network into several ring-shaped structures, where each node in the ring maintains its own data and routing information for other nodes in the network using the Chord DHT. Communication between nodes in the same ring is possible, while communication between different rings requires specific routing nodes.

The advantage of Rings Network is its lightweight nature, as it does not require consensus calculations, making it capable of supporting a large number of nodes (2^160). The use of the Chord DHT in Rings Network enables data to be stored and retrieved in a distributed manner, allowing for decentralized storage and DWeb. It also allows for the creation of hidden services, which can be useful for anonymity and privacy. Additionally, DHT allows for the lookup of nodes in the network which can be used for different types of routing and communication.

Rings Network is designed to be a communication layer for the Sovereign Age of the internet, and as such, it utilizes end-to-end encryption to protect the privacy of users. This makes it possible to implement various advanced cryptographic techniques such as interactive zero-knowledge proof (IZK), atomic-swap, and secret-sharing (SSSS).

Interactive zero-knowledge proof (IZK) allows for the verification of information without revealing the underlying data. Atomic-swap is a technique that allows for the exchange of one cryptocurrency for another without the need for a trusted third party. Secret-sharing (SSSS) is a technique that allows for the secure sharing of sensitive information among multiple parties. The end-to-end encryption of Rings Network enables these cryptographic techniques to be used in a decentralized and trustless manner.





