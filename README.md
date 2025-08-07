Steps to reproduce:

> Has `experimental.cacheComponents` enabled.

```
pnpm i && pnpm build
```

Receive the following error:

```
Route "/dynamic/[id]" has a `generateMetadata` that depends on Request data (`cookies()`, etc...) or uncached external data (`fetch(...)`, etc...) when the rest of the route does not. See more info here: https://nextjs.org/docs/messages/next-prerender-dynamic-metadata
Error occurred prerendering page "/dynamic/[id]". Read more: https://nextjs.org/docs/messages/prerender-error
Export encountered an error on /dynamic/[id]/page: /dynamic/[id], exiting the build.
 ⨯ Next.js build worker exited with code: 1 and signal: null
```