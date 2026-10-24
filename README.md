# Pidlock

Pidlock is the user-owned, consent-first data vault for **Share the Value**, an open protocol by Akbar Lalani.

> Status: early draft, v0.2. Everything here is open for discussion.

## What is Share the Value?

Share the Value is an open specification anyone can implement. It describes how consent, matching, attribution and payouts work between a person, a platform and a merchant.

Personal data helps platforms and merchants reach the right people and make sales. The people whose data makes that possible rarely see any of the value, and they often have little say over who sees what. Share the Value proposes a simple, open way to change that, working alongside the platforms people already use rather than against them.

## What is Pidlock?

Pidlock is the person's vault. PID means personally identifiable data. Pidlock keeps it locked, and shares it only with consent.

- Your data stays on your own device.
- You can switch access on or off for each company at any time.
- Businesses never receive your raw data.

## How the protocol works

![Share the Value protocol flow](https://sharethevalue.org/images/protocol-flow.gif)

- **Coexists with big tech.** The platform keeps the majority share; the person receives a fraction.
- **Cash first.** Payouts come as cash first, with credits as an option later.
- **Verified sales only.** Payouts happen only on verified sales that are not returned.
- **Measured, not assumed.** Lift is measured against a holdout group.
- **Nothing breaks.** Existing ads continue as normal for people who do not opt in.

## Who benefits

These are what we expect. A pilot is how we will find out.

- **Platforms** keep the majority share, offer a consent-based option people may prefer, and coexist with existing ads.
- **Merchants** pay only for verified, unreturned sales, with lift measured against a holdout group.
- **People** choose who sees what, keep data on their device, and receive a fair share when their data helps.

## The pilot

The first step is a pilot with one challenger platform. The aim is to test, with real numbers and a holdout group, whether this works well for platforms, merchants and people alike. Results will be shared openly.

## Status and roadmap

This is a proposal at an early stage. Nothing here is built yet. We plan to move in three stages.

**Stage 1: Feedback and early supporters.** Share the specification and the article, gather feedback, and find people who think the idea is worth testing.

**Stage 2: Contributors and design partners.** Find two or three serious contributors or design partners to shape the first build.

**Stage 3: A working demo.** Build a demo that a platform or merchant could try for themselves.

Starter build items:

- A reference implementation of scoped, revocable keys for the Pidlock vault.
- A demo of an AI agent sending a user's intent to a mock platform.
- A test suite and conformance checks so others can verify their own implementations.

## Who is behind this

Akbar Lalani proposed the Share the Value protocol and stewards it. He sets the direction and the principles. He is not a hands-on engineer, and he builds with AI assistance, openly. Contributors are welcome, and the project will rely on people with skills he does not have.

## How to help

- **Developers:** help build the starter items above, starting with scoped keys, the agent demo, or the test suite.
- **Designers:** help make consent, key revocation and payouts clear and simple for people.
- **Payments people:** help shape how payments, returns and payouts to people should work in practice.
- **Policy people:** help review how the protocol fits with the EU Digital Markets Act and GDPR. Any alignment is subject to legal review.

Open an issue on this repository to ask a question, suggest a change, or say what you would like to work on. See [CONTRIBUTING.md](CONTRIBUTING.md) for more.

## Related work

Share the Value builds on ideas and standards that already exist. Each piece has precedent; the combination is what we are proposing.

- **Intent and user-side terms:** [ProjectVRM and The Intention Economy](https://cyber.harvard.edu/projectvrm/Main_Page) (Doc Searls), [Customer Commons](https://customercommons.org/), [IEEE 7012 machine-readable personal privacy terms](https://standards.ieee.org/ieee/7012/7192/), [Kantara Consent Receipt](https://kantarainitiative.org/download/7902/).
- **Personal data stores:** [Solid](https://solidproject.org/), [MyData](https://mydata.org/), [digi.me](https://digi.me/).
- **Paying people for attention or data:** [Brave Rewards](https://brave.com/brave-rewards/), data unions such as [Swash](https://swashapp.io/) and [Streamr](https://streamr.network/), and the earlier [Datacoup](https://www.technologyreview.com/2014/09/08/171469/datacoup-wants-to-buy-your-credit-card-and-facebook-data/).
- **Economics:** [Should We Treat Data as Labor?](https://www.aeaweb.org/articles?id=10.1257/pandp.20181003) and [A Blueprint for a Better Digital Society](https://hbr.org/2018/09/a-blueprint-for-a-better-digital-society).
- **Agent commerce and authorization:** [Agent Payments Protocol (AP2)](https://ap2-protocol.org/), [Agentic Commerce Protocol (ACP)](https://www.agenticcommerce.dev/), [Visa Intelligent Commerce](https://corporate.visa.com/en/products/intelligent-commerce.html), [GNAP (RFC 9635)](https://datatracker.ietf.org/doc/rfc9635/).

What we think is new: an AI agent shares only consented intent from a vault on the user's device, and the user's share comes from the platform's commission on a verified sale, paid after the return window. We have not found another project that ties a user payout to a completed purchase. If you know of one, please open an issue.

## Links

- Website: https://sharethevalue.org (coming soon)
- White paper: [docs/paper.md](docs/paper.md)
- How to help: [CONTRIBUTING.md](CONTRIBUTING.md)

## License

- Code: [Apache License 2.0](LICENSE)
- Docs, paper and specification: [CC BY 4.0](LICENSE-docs)

Share the Value, by Akbar Lalani.
