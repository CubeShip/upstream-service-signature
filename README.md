# upstream-service-signature
a kong gateway plugin,support generate signature for upstream service authentication.

### Summary

By specified algorithm,generate signature information and add them in request header for upstream service authentication,in order to protect upstream API security.

### signature algorithm

- signature content structure： signature_key=[signature_key]&signature_time=[signature_time], signature_key and signature_time participate in signature, signature_time is current UTC timestamp
- base64_safe(HMAC-SHA1(signature_secret, signature_str)) generate signature