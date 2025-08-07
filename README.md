Next Info:

```
Node.js v20.18.0

Operating System:
  Platform: darwin
  Arch: arm64
  Version: Darwin Kernel Version 24.6.0: Mon Jul 14 11:28:30 PDT 2025; root:xnu-11417.140.69~1/RELEASE_ARM64_T6030
  Available memory (MB): 36864
  Available CPU cores: 12
Binaries:
  Node: 20.18.0
  npm: 10.8.2
  Yarn: N/A
  pnpm: 8.15.9
Relevant Packages:
  next: 15.4.2-canary.32 // Latest available version is detected (15.4.2-canary.32).
  eslint-config-next: N/A
  react: 19.1.0
  react-dom: 19.1.0
  typescript: 5.9.2
Next.js Config:
  output: N/A
```

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