# Set tis rule at Rules -> Transform rules -> Modify Response header: rules/transform-rules/modify-response-header

## Rule name:

- Rules Author

## Custom filter expression:

- (http.request.uri contains "")

## Then (Header action, Header Name, Header Value)
- Set Static
- x-cl-rules-author
- `https://jclc.me/codeable`
