# Removal of Rate Limit Response headers

## Products affected
- [ ] SDK
- [x] API
- [ ] Admin UI
- [ ] Nodes
- [ ] Servers

## Is this a breaking change?
- [x] yes
- [ ] no

## Description of the change

For the purpose of optimization, rate limiting and throttling will now be handled asynchronously in such a way that the following will no longer be available in the response headers:
- x-rate-limit-remaining-ttl
- x-rate-limit-remaining-ip-ttl
- x-rate-limit-used
- x-rate-limit-ip-used
- x-rate-limit-limit
- x-rate-limit-throttle-remaining-ttl
- x-rate-limit-throttle-remaining-ip-ttl
- x-rate-limit-throttle-used
- x-rate-limit-throttle-ip-used
- x-rate-limit-throttle-limit
- x-rate-limit-remaining-ttl
- x-rate-limit-remaining-ip-ttl
- x-rate-limit-used
- x-rate-limit-ip-used
- x-rate-limit-limit



## What exactly can break?

If you rely on these response headers to adjust your request rate, you may experience issues.

## How to ensure my app won't break?

Rather than adjusting request rate based on the headers returned, your code should instead rely only on the http error response 429 "Rate Limit exceeded". 

## When will this change go live and be mandatory?

2022-09-06

## Link to Moralis Forum for discussions

https://forum.moralis.io/t/removal-of-rate-limit-response-headers-on-sept-6-2022/18873


