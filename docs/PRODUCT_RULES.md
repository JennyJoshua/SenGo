# SenGo Product Rules

**Status:** Owner-approved product direction, subject to legal and technical validation where stated.

## 1. Product purpose

SenGo is a Papua New Guinea-first peer-to-peer logistics marketplace connecting people who need packages transported with independent travellers who have available capacity on journeys they are already making.

**Positioning:** Your journey can deliver more.

SenGo is initially a marketplace, not a transport operator. It does not own or operate a fleet in the MVP.

## 2. Business model

- Free user onboarding.
- Senders and independent travellers transact directly.
- SenGo records delivery agreements and reported payment status.
- SenGo does not initially hold funds, provide escrow or operate a wallet.
- A controlled pilot precedes national expansion.

Any future commissions, paid business services or payment integrations require separate commercial, legal and owner review.

## 3. User roles

### Sender
Creates a delivery request, declares package details and restrictions, reviews matches, and agrees terms with a traveller.

### Traveller
Creates a travel intention, declares transport mode and available capacity, reviews opportunities and accepts or declines delivery agreements.

### Receiver
Is designated to receive the package and must confirm receipt for a delivery to reach the completed state.

### Administrator
Manages verification, safety reports, disputes, platform configuration and operational oversight.

A person may act as both sender and traveller. Role permissions must be enforced by trusted server/database controls.

## 4. Transport modes

The system is designed to represent:

- Road
- Sea
- Air
- Walking

Each mode requires its own eligibility, safety, prohibited-goods and regulatory controls. A mode can be disabled independently. Architecture support does not mean that a mode is legally approved for commercial use.

## 5. Travel intentions

A traveller may publish a public or private journey.

- Public journeys may appear in public discovery.
- Private journeys must not appear in public search results.
- Private journeys may be considered by the private matching process.
- Private journey details must not be exposed to a sender until the relevant traveller consents and the workflow permits disclosure.

## 6. Delivery requests

A request should capture, as applicable:

- Origin and destination.
- Intermediate route preferences.
- Package category and description.
- Declared weight and dimensions.
- Package images or evidence where justified.
- Required delivery date/deadline.
- Offered fee and currency.
- Receiver contact/identity details appropriate to the workflow.
- Prohibited/restricted item declarations.

The platform must not imply that user declarations replace required physical checks, carrier rules or legal requirements.

## 7. Matching

The initial matching engine is deterministic and must consider:

- Origin/destination and route compatibility.
- Intermediate stops.
- Travel dates and delivery deadline.
- Available carrying capacity.
- Transport mode and mode-specific restrictions.
- Package category and restricted-goods rules.
- Verification and eligibility status.
- Journey status and visibility.

Matching must not expose private journey details prematurely. Paid AI services are not required for the MVP.

## 8. Delivery agreements

Before package handover, sender and traveller must both accept an agreement describing the package, route, delivery expectations, fee, transport mode, declarations and applicable responsibilities.

Changes after acceptance must be recorded and re-accepted where they materially affect the agreement.

## 9. Custody and delivery completion

The delivery record must support the following concepts:

1. Agreement accepted.
2. Sender hands package to traveller.
3. Traveller confirms custody.
4. Package is in transit.
5. Traveller records arrival/ready for collection.
6. Receiver confirms receipt.
7. Delivery is completed.

The receiver's confirmation is required. A traveller must not unilaterally mark a package delivered. Every important custody event must be attributable and timestamped.

## 10. Payments

- Sender and traveller agree the fee directly.
- SenGo records the agreed amount and reported status.
- Reported payment must not be represented as independently verified unless a future approved verification mechanism exists.
- No wallet, escrow or SendGo-held funds in the MVP.

## 11. Safety and administration

The product must support prohibited/restricted goods controls, reporting, identity verification, dispute handling, evidence protection and audit logging.

## 12. MVP exclusions

The initial MVP excludes:

- SenGo-owned vehicles, boats, aircraft or courier workforce.
- Wallet, escrow or SendGo-held funds.
- Multi-traveller package handoffs.
- Automated GPS tracking.
- International shipping.
- AI-based people, job or dating matching.

## 13. Legal and launch constraint

No feature description in this document constitutes legal clearance. Postal/letter delivery, road carriage, maritime transport, aviation, dangerous goods, privacy, consumer protection, liability and payments require appropriate assessment. Commercial activation of a transport mode is gated on documented review and owner approval.
