# Restructure JS SDK API result

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

For any api call, you get a resultAdapter response. The value of the `toJSON()` value has changed. Now it is the same value as `.raw`. Previously this caused a lot of confusion, and as both return a json. The value of this method has changed. So if you used `.toJSON()` on an api result you can:

- Use `.result`, this will probably contain dataTypes with lots of utility functions. If you only care about the data, you can call `.format()` or `.toJSON()` on this datatype. This is the prefered way as it provides you wilt additional utilites and extra properties. We suggest you to use Typescript, to easily see the available properties/methods on these datatypes.

- Or. use the new values (or values from `.raw`), these values are identical as they are provided by the internal api, without any data transformation. The types might be different than before, so please check this (we suggest to use Typescript, as all responses are typed, otherwise you can log the output and see any differences)
 
## What exactly can break?

The value of the `.toJSON()` on api results in the JS SDK

## How to ensure my app won't break?

Postpone updating the SDK until:
- You verified that you still get the correct results
- Prefer changing the `.toJSON()` to `.result` (if you want to use all properties) or `.raw` (if you only need the raw data from the api)

## When will this change go live and be mandatory?

28-11-2022

## Link to Moralis Forum for discussions

https://forum.moralis.io/t/restructure-js-sdk-api-result-from-28-november-2022/21140

## Code Examples

Give as many code examples as possible for different scenarios.

```javascript
const { result, raw } = await Moralis.EvmApi.block.getBlock({
  blockNumberOrHash: '15305775',
  chain: EvmChain.Ethereum,
});

// In this case the result is a datatype: EvmBlock, so we can use the toJSON() method on this datatype
const block = result.toJSON();

// Alternatively, the .raw value can be used, but the types and property names might differ a bit
const apiData = raw
```


```javascript
const { result, raw } = await Moralis.EvmApi.token.getTokenPrice({
  address: '0x1234567890123456789012345678901234567890',
  chain: EvmChain.Ethereum,
});

// In this case the result does not return a datatype directly, but rather an object with properties as 'nativePrice' and 'exchangeAddress'. To get serializable values you can call:
const price = result.nativePrice.format()
const exchangeAddress = result.exchangeAddress.format()

// Alternatively, the .raw value can be used, but the types and property names might differ a bit
const apiData = raw
```

## Best practices

Update to the new version of the SDK if:
- You have verified the places where apiResult.toJSON() is used
- Change the value to `.result` or `.raw`
- Use Typescript to ensure the property names and types are correct
