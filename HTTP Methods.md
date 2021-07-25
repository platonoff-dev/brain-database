HTTP methods #Web #ClientServer #Backend #Protocols

Thing that actively used in [[Web development]] now. Because HTTP/HTTPS on the top now.

| Method | Idempotency | Safety |
|---|---|---|
| GET | [x] | [x] |
| OPTIONS |	[x] | [x] |
| HEAD | [x] | [x] |
| PUT |	[x] | [ ] |
| POST | [ ] | [ ] |
| PATCH | [ ] | [ ] |
| DELETE | [x] | [ ] |


Safety means that request doesn't change server state.

Idempotency means that request may be called multiple times and all result will be identically.