## 44Billion

[44Billion.net](https://44billion.net) is a website that
presents itself as a thin layer, a toolbar where
the Nostr apps you install are placed.

#### Initial View

One of the initial apps is an app store.

<img width="495" height="501" alt="0-init-view" src="https://github.com/user-attachments/assets/5620ddfb-1268-43ad-9cdd-8972626ccc41" />

#### App Store

The app store is there to help the user discover and install new Nostr apps.

<img width="495" height="501" alt="2-app-store" src="https://github.com/user-attachments/assets/76370969-26d8-4c4f-9909-3c69c7a1399a" />

#### Account Creation

The account creation is very straightforward. Pick an avatar and a name.

<img width="495" height="501" alt="3-create-account" src="https://github.com/user-attachments/assets/f0d60439-87b9-4695-adb8-46daed37ce2f" />

#### Account Syncing

The nsec is encrypted and synchronized across devices by using passkeys. Existing nsecs can be imported as well.

<img width="495" height="501" alt="4-synced-passkeys" src="https://github.com/user-attachments/assets/73402d40-5bfa-4f01-b8b1-0439168ba007" />

#### All apps have access to `window.nostr`

When opening an app, the user is already logged-in there.

<img width="495" height="501" alt="5-auto-login" src="https://github.com/user-attachments/assets/826b0dc4-2709-473a-9855-7e36fb290a02" />

### Free relay for our users and everyone else

We have a free and spam-resistant relay too at wss://relay.44billion.net. Open-source code: [https://github.com/44Billion/44b-relay](https://github.com/44Billion/44b-relay). While we're at it, also check the core platform code: [https://github.com/44Billion/44billion](https://github.com/44Billion/44billion), the signer module repo: [https://github.com/44Billion/44b-vault](https://github.com/44Billion/44b-vault) and the app store [https://github.com/44Billion/nappstore](https://github.com/44Billion/nappstore)

### Boring Details

- Apps files are stored on Blossom.
- App manifest (NIP-5A) and app listing (NIP-5B) events on relays.
- Anyone can publish an app without asking and it shows on the app store.
- Login is handled by a signer that lives on a separata domain: Github Pages by default.
- 44billion.net can't access your nsec directly and you may even self-host the signer.

### Cool Detail

Apps are installed locally. It allows you to control if and when to update them:

<img width="422" height="629" alt="6-local-apps" src="https://github.com/user-attachments/assets/8a33632c-e576-4864-bc2d-9a30c6713338" />
