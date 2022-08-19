# Title of the change and version

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

For the purpose of optmization, rate limiting and throttling will now be handled asynchronously in such a way that the following will no longer be available in the response headers:
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

2022-08-19

## Link to Moralis Forum for disucssions

Create a thread in Moralis forum in this category (https://forum.moralis.io/c/changelog/20) and name the thread with the same TITLE as this MR and link it here

We have staff monitoring forum 24/7 - while we don't monitor github as much - so we need everyone to discuss in the forum

## Code Examples

Give as many code examples as possible for different scenarios.

## Best practices

Explain best practices
