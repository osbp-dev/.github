# Open Service Booking Protocol (OSBP)

OSBP is an open protocol layer for AI-assisted service booking. It lets an
agent book an appointment only inside a scoped, user-approved authorization
called a `BookingMandate`.

```text
Customer <-> AI agent <-> OSBP server <-> booking platform
```

MCP carries the transport. OSBP defines the booking tools, mandate validation,
failure shape, and audit expectations around a provider-bound appointment.

## Start here

- **Canonical site:** [osbp.dev](https://osbp.dev)
- **Specification and reference implementation:** [osbp-dev/osbp](https://github.com/osbp-dev/osbp)
- **Versioned spec:** [v0.1.0](https://osbp.dev/spec/v0.1.0/)
- **Local demo:** run `npm run demo` in `osbp-dev/osbp`
- **Contributing:** see `CONTRIBUTING.md` in the main repo

## v0.1.0 status

[![latest release](https://img.shields.io/github/v/release/osbp-dev/osbp?label=release)](https://github.com/osbp-dev/osbp/releases)
[![released](https://img.shields.io/github/release-date/osbp-dev/osbp?label=shipped)](https://github.com/osbp-dev/osbp/releases)

v0.1.0 is a usable proof and formative contract, not a production maturity
claim. It demonstrates one small booking loop:

```text
BookingMandate -> lookup -> policy readback -> user approval -> create -> verification if required -> status -> receipt
```

The public cut includes protocol docs, a TypeScript protocol core, a local
stdio MCP server, a credential-free synthetic reference backend, trace tooling,
a conformance kit, an adapter starter, and an optional Openings integration
proof for an operator-owned business.

It does not include payments, marketplace search, slot holds, modify/cancel
flows, production mandate signing, public conformance certification, or a
universal adapter promise.

OSBP authorizes the booking, not the payment.

## Licensing

Code is licensed under Apache-2.0. Specification prose and documentation are
licensed under CC-BY-4.0 unless a file states otherwise.
