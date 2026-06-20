# Open Service Booking Protocol (OSBP)

An open protocol that lets an AI agent book a real service appointment, but only
inside a scoped, user-approved authorization called a `BookingMandate`.

```text
Customer <-> AI agent <-> OSBP <-> booking platform
```

Communication is bidirectional; authority is directional. Every booking action
stays inside what the customer approved.

OSBP is an open standard, first published in 2026 by [Andy Volk](https://andyvolk.com/).
Background and rationale: [osbp.dev](https://osbp.dev).

## Start here

- **Read the spec** — the normative contract: tools, mandate enforcement, audit, and time discipline. [osbp-dev/osbp](https://github.com/osbp-dev/osbp)
- **Try it, no credentials** — a reference backend with four synthetic verticals runs the full booking loop locally.
- **Write an adapter** — map your booking platform to OSBP with the starter kit, then prove it against the conformance kit.
- **Contribute** — see `CONTRIBUTING.md` in the main repo.
- **Why this exists** — [osbp.dev](https://osbp.dev)

## Status

[![latest release](https://img.shields.io/github/v/release/osbp-dev/osbp?label=release)](https://github.com/osbp-dev/osbp/releases)
[![released](https://img.shields.io/github/release-date/osbp-dev/osbp?label=shipped)](https://github.com/osbp-dev/osbp/releases)

Works end to end against a real booking platform and a credential-free reference
backend. The release above tracks what is shipped; the contract is formative and
breaking changes are expected until it stabilizes.

OSBP authorizes the booking, not the payment. It is designed to compose with the
payment-authority layers converging separately.
