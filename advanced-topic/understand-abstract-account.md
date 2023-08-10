# Understand Abstract Account

The Rings network offers a unique mechanism to bolster security and abstract the user's keypair through a feature known as session keypair.

The fundamental concept behind keypair session involves creating an association between a user's keypair and a randomly generated keypair. In our terminology:&#x20;

* The user's original keypair (private key, public key) is referred to as the "account" (sk, pk).
* The randomly generated keypair by the Rings network is known as the "session" (sk, pk).

### Here's how the process works:&#x20;

1\. A random delegate private key (sk) is generated, along with its corresponding public key (pk).&#x20;

2\. A session is formed based on the session's public key and the account's public key. This can be conceptualized as a contract stating, "I delegate to {pk} for the time period {ts, ttl}".

3\. The account must sign the session, now termed "Session", using its private key.&#x20;

4\. When sending and receiving messages, the Rings network will handle message signing and verification using the session's keypair (sk, pk).



`SessionSkBuilder`, `SessionSk` was exported to wasm envirement, so in browser/wasm envirement it can be done with nodejs code:

````
//! ```js
//!    // prepare auth & send to metamask for sign
//!    let sessionBuilder = SessionSkBuilder.new(account, 'eip191')
//!    let unsignedSession = sessionBuilder.unsigned_session()
//!    const { signed } = await sendMessage(
//!      'sign-message',
//!      {
//!        auth: unsignedSession,
//!      },
//!      'popup'
//!    )
//!    const signature = new Uint8Array(hexToBytes(signed))
//!    sessionBuilder = sessionBuilder.set_session_sig(signature)
//!    let sessionSk: SessionSk = sessionBuilder.build()
//! ```
````



&#x20;

