---
default: patch
---

# Expose the retry pushback to browser (gRPC-web) clients

With `[serve] grpc_web = true`, a refusal's `grpc-retry-pushback-ms` is now listed in
`Access-Control-Expose-Headers` next to `grpc-status` and `grpc-message`, so a browser wallet can
read it and wait as long as the server asks.
