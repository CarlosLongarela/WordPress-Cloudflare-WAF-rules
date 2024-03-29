# Set tis rule at Rules -> Transform rules -> Modify Response header: rules/transform-rules/modify-response-header

## Rule name:
- Add Security headers

## Custom File Expression:
- (http.request.uri contains "" and not http.request.full_uri contains ".css" and not http.request.full_uri contains ".js" and not http.request.uri contains ".jpg" and not http.request.uri contains ".gif" and not http.request.uri contains ".png" and not http.request.uri contains ".webp")

## Then (Header action, Header Name, Header Value)
- Set Static
- Content-Security-Policy
- frame-ancestors 'self'

---

- Set Static
- access-control-allow-credentials
- true

---

- Set Static
- access-control-allow-headers
- \*

---

- Set Static
- access-control-allow-methods
- GET, POST, OPTIONS

---

- Set Static
- access-control-allow-origin
- \*

---

- Set Static
- permissions-policy
- accelerometer=(), autoplay=(), camera=(), cross-origin-isolated=(), display-capture=(), document-domain=(), encrypted-media=(), fullscreen=(self), geolocation=(), gyroscope=(), magnetometer=(), microphone=(), midi=(), payment=(), picture-in-picture=(), publickey-credentials-get=(), screen-wake-lock=(), sync-xhr=(self), usb=(), web-share=(), xr-spatial-tracking=()

---

- Set Static
- referrer-policy
- strict-origin-when-cross-origin

---

- Set Static
- x-permitted-cross-domain-policies
- none
