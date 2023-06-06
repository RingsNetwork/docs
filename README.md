# Introduction

<figure><img src="https://camo.githubusercontent.com/1e8e8235037707bbdc8e2a24242e5874b8be89b971f0ae552585b46398971b6f/68747470733a2f2f7374617469632e72696e67736e6574776f726b2e696f2f72696e67736e6574776f726b5f6c6f676f2e706e67" alt=""><figcaption></figcaption></figure>

Rings Network is a purely peer-to-peer network implementation. We use WebRTC to establish peer connections, and use WebAssembly to allow nodes to run in the browser. Rings Network uses the DHT (Chord) algorithm for message routing/addressing.

By introducing decentralized PKI (public key infrastructure) such as Ethereum and Bitcoin, we have built a series of cryptographic-based network infrastructures. For example, we support end-to-end and hop-by-hop encryption systems, service discovery and registration systems based on resource hashes, and so on.

## # Getting Start

Rings Network is being built with the Rust language. We compile the code into WASM or Native to meet the needs of different scenarios. To better understand Rings Network, we recommend that you start with the Native Node.

#### Start with Native Node

Before Getting Start, Rust is required, follow the [official instructions](https://www.rust-lang.org/tools/install).

[getting-started.md](getting-started.md "mention")

#### Start with Wasm Node

[build-for-wasm.md](build-for-wasm.md "mention")

## # Architecture

The Rings Network architecture is streamlined into five distinct layers.

&#x20; For more details, please check [architecture.md](advanced-topic/architecture.md "mention")

