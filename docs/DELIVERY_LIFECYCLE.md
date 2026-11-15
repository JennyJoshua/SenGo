# SenGo Delivery Lifecycle

This is the product-level lifecycle baseline. The exact database representation and state-machine implementation will be designed in a later issue.

## Expected sequence

```text
REQUEST_CREATED
      |
      v
MATCHED
      |
      v
AGREEMENT_PENDING
      |
      v
AGREEMENT_ACCEPTED
      |
      v
AWAITING_SENDER_HANDOVER
      |
      v
TRAVELLER_IN_CUSTODY
      |
      v
IN_TRANSIT
      |
      v
ARRIVED_AWAITING_RECEIVER
      |
      v
RECEIVER_CONFIRMED
      |
      v
DELIVERED
```

## Rules

1. A match is only a candidate; it does not create a delivery agreement.
2. Both sender and traveller must accept the agreement before handover.
3. A package cannot enter traveller custody until the authorised handover step is confirmed.
4. Custody events must identify the actor, event type and timestamp.
5. A traveller cannot independently mark a delivery completed.
6. Receiver confirmation is required for the delivered state.
7. Cancellation, failed handover, loss, damage and dispute paths must be defined before production implementation.
8. State transitions must be enforced server-side and tested against invalid transitions.
9. A QR code or tracking reference must not reveal private personal information.
10. The lifecycle does not imply that every transport mode or package category is legally authorised.

## Outstanding design work

The later technical design must define:
- Exact enum/state names.
- Permitted transitions and transition guards.
- One-time code issuance, expiry, retries and rate limits.
- Receiver verification and exception handling.
- Cancellation and dispute transitions.
- Event immutability and audit retention.
