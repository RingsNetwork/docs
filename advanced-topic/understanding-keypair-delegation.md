# Understanding Keypair Delegation

The Rings network offers a unique mechanism to bolster security and abstract the user's keypair through a feature known as keypair delegation.

The fundamental concept behind keypair delegation involves creating an association between a user's keypair and a randomly generated keypair. In our terminology:

* The user's original keypair (private key, public key) is referred to as the "delegator" (sk, pk).
* The randomly generated keypair by the Rings network is known as the "delegatee" (sk, pk).

Here's how the process works:

1. A random delegate private key (sk) is generated, along with its corresponding public key (pk).
2. A delegation is formed based on the delegatee's public key and the delegator's public key. This can be conceptualized as a contract stating, "I delegate to {pk} for the time period {ts, ttl}".
3. The delegator must sign the delegation, now termed "Session", using its private key.
4. When sending and receiving messages, the Rings network will handle message signing and verification using the delegatee's keypair (sk, pk).

DelegateeSkBuilder, DelegateeSk was exported to wasm envirement, so in browser/wasm envirement it can be done with nodejs code:

```
    // prepare auth & send to metamask for sign
    let delegateeBuilder = DelegateeSkBuilder.new(account, 'eip191')
    let unsignedDelegation = delegateeBuilder.unsigned_delegation()
    const { signed } = await sendMessage(
      'sign-message',
      {
        auth: unsignedDelegation,
      },
      'popup'
    )
    const signature = new Uint8Array(hexToBytes(signed))
    delegateeBuilder = delegateeBuilder.set_delegation_sig(signature)
    let delegateeSk: DelegateeSk = delegateeBuilder.build()
```



&#x20;

