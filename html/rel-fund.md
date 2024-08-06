
# `rel=fund`

As ad-blockers have become the norm, authors may choose for more of an opt-in approach to monetization of their online content. In an attempt to somewhat standardize the way end-users can find the preferred method(s) of supporting their favorite creators, I propose a new and dedicated link relation.

## Examples

Link to a [Patreon](https://www.patreon.com/acj) profile  (in conjunction with [`rel=me`](https://microformats.org/wiki/rel-me)).

```html
<link rel="fund me" href="https://www.patreon.com/acj">
```

Send a Bitcoin using [BIP 0021](https://en.bitcoin.it/wiki/BIP_0021).

```html
<link rel="fund" href="bitcoin:1EuDRzJ1K2owkLQv6Y85mc8kqCd7JHfgh8?amount=1">
```

Utilizing the [Brave Reward System](https://brave.com/brave-rewards/) (using [Basic Attention Tokens](https://basicattentiontoken.org/)).

```html
<link rel="fund" href="https://example.com/.well-known/brave-rewards-verification.txt">
```
