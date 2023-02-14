# Set tis rule at Rules -> Transform rules -> Modify Response header: rules/transform-rules/modify-response-header

## Rule name:

- Remove link header

## Custom filter expression:

- (http.request.uri contains "" and not http.request.full_uri contains ".css" and not http.request.full_uri contains ".js" and not http.request.uri contains ".jpg" and not http.request.uri contains ".gif" and not http.request.uri contains ".png" and not http.request.uri contains ".webp")

## Then: 

### Set Header:
- Remove

### Header Name:
- link
