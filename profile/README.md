## 44Billion

[44Billion](https://44billion.net) is a `napp launcher`.
It is a website where you can discover and launch
micro Nostr webapps, called `napps`, for short.

A `napp` is a good ol' static website bundled as a Nostr event.
Each of its files is split into tiny chunk events, all signed by the author.

A `napp launcher` is expected to handle all the boring multi-account
sign in/up flow and make the
[NIP-07](https://github.com/nostr-protocol/nips/blob/master/07.md)'s
`window.nostr` object available to the napps.

### Auto-Login

Napps can use the new `await window.nostr.peekPublicKey()` method
to learn who is the logged-in user.

The classic `getPublicKey` function is still there,
but it was created to prompt the user for confirmation, while
`peekPublicKey` is expected to be available when auto-login is on,
which is the default when using a napp launcher.

### Napp Discovery

`Napp stores` are regular napps focused on helping users discover
new napps.

They are also used to upload dev's static websites to
automatically make them become napps, **without any prior code
adaptation**.

### Security

44Billion pioneered a way of securely storing and
managing Nostr privkeys, that is specially thought for
non tech savvy users, while being self-hostable
for those that want more control.
[Learn more](https://github.com/44Billion/44b-vault).

### Why was This Created?

User onboarding and retention. There's a whole world of differences between
simply listing separate nostr webapps links like on
[nostrapps.com](https://nostrapps.com/)
and providing a cohesive platform like [44Billion](https://44billion.net)
that holds user hands at every step they take, including login, keys backup,
app pinning and soon user data backup among other amenities.

44Billion turns webapps into instantly loaded, offline-first,
`window.nostr` enhanced napps, permissionlessly discoverable on napp stores.

Last but not least, manual napp updates! This solves a
[long standing problem with webapps](https://njump.me/naddr1qvzqqqr4gupzqwlsccluhy6xxsr6l9a9uhhxf75g85g8a709tprjcn4e42h053vaqyf8wumn8ghj7enfv96x5ctx9e3k7mf0qqyrvwpj89skgwrz0upj9h).

All this with a thin overlay user interface that doesn't get in the way of the user.
The user won't notice the complexity running behind the scenes.

### Development Backlog

Progress overview: 4 / 18 completed

#### ✅ Completed
- [x] Basic app dock
- [x] Multi-account support
- [x] Multi-window support
- [x] External Login Module

#### 🧱 Core Platform
- [ ] App update management
- [ ] Custom Login Module selection
- [ ] App embedding (enable a napp to load other napps)
- [ ] Human-readable napp names (aliases)
- [ ] Polish UI

#### 🛍 Napp Discovery & Distribution
- [ ] App store napp (upload, categories, reviews) — only a simple demo exists today

#### 🧩 Built-in / Starter Napps
- [ ] Basic short-notes napp
- [ ] Basic messenger napp

#### 🌐 Relays & Data Flow
- [ ] Free Public Relay
- [ ] Free Outbox Relay to expose events on user's local DB (novel approach)

#### 🔐 Cryptography & Security
- [ ] Signer Security Add-Ons
- [ ] [TOFU](https://developer.mozilla.org/en-US/docs/Glossary/TOFU) for app secondary signing key
- [ ] FROST support

#### 📈 Quality & Reliability
- [ ] Increase Test Coverage
