# Host a Native Node

After installation, you can create your configuration by:

```bash
rings init
```

This command will generate a configuration file named config.yaml for you. The default path is $HOME/.rings/config.yaml. You can also customize the path by using `rings init --location <path>`. Additionally, you can specify the key used by the Rings node by using `rings init -k <your private key>`.

By default, an ECDSA key pair will be automatically generated for you. The key pair in Rings Network is used for user identification and message signing. The key pair is utilized in various components of the network, so it is essential for users to ensure the security of their key pair. In the Native Node environment, since the private key is stored in plaintext, we strongly **discourage** the use of any asset-related key pair to host Rings Network.

Here is an example of how your config.yaml file might look:
