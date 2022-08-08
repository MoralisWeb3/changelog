# moralis-v1 support

## Products affected
- [x] SDK
- [ ] API
- [ ] Admin UI
- [ ] Nodes
- [ ] Servers

## Is this a breaking change?
- [x] yes
- [ ] no

## Description of the change

With Moralis2.0 we will focus on backend SDKs. This means that the new version of the JS SDK will only support NodeJs (no browser or react-native). To continue supporting the current v1 version we forked the repo to `moralis-v1` (see https://github.com/MoralisWeb3/Moralis-JS-SDK-v1). This version will receive bug-fixes, small updates and security patches.

## What exactly can break?

Updating to v2 of the SDK will drop support for client-side functionalities, server interactions and plugins. It will **not break** if you have a version specified (not using @latest).

## How to ensure my app won't break?

If you are using npm (and v1.11.0), you should switch the library from `moralis` ro `moralis-v1`.

If you are using a CDN import via a `<script>`  (and v1.11.0) then you should update it from `https://unpkg.com/moralis@1.11.0/dist/moralis.js` to `https://unpkg.com/moralis-v1@1.11.0/dist/moralis.js`.

Note that this only applies if you are using the latest version of the SDK or want to update to a version of 1.11 or above. Otherwise you can leave the version as it is right now, and update to `moralis-v1` when you upgrade to the latest version.

## When will this change go live and be mandatory?

2022-08-10

## Link to Moralis Forum for disucssions

https://forum.moralis.io/t/moralis-v1-support-august-8-2022/18383

## Code Examples

For npm users
```sh
npm remove moralis
npm install moralis-v1
```

```javascript
// Old
import moralis from 'moralis'
// New
import moralis from 'moralis-v1'
```

For CDN users
```html
<!-- Old -->
<script src="https://unpkg.com/moralis@1.11.0/dist/moralis.js">
<!-- New -->
<script src="https://unpkg.com/moralis-v1@1.11.0/dist/moralis.js">

```
## Best practices
- Never use `@latest` versions in production code, as this may result in breaking changes when moralis updates to v2.
- The best practice is to update your dependency to `moralis-v1` as soon as possible. The code of v1.11.0 is exactly the same as `moralis` v1.11.0. 
- If you are using Moralis mainly in NodeJs, then consider updating moralis to v2, once it is published.