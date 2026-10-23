# Share the Value and Pidlock

**Summary draft, full paper to follow**

Author: Akbar Lalani
Status: early draft, v0.2

> This document summarises the white paper. The full paper will replace it once it is published. Feedback is welcome through issues and discussions.

## 1. Problem

Personal data helps platforms and merchants reach the right people and make sales. The people whose data makes that possible rarely see any of the value, and they often have little say over who sees what, or where their data goes.

Sharing personal data is not always a bad thing. Used with consent, it can make services more relevant. The goal is not to stop it, but to put the person in control and let them share in the value it helps create.

## 2. Share the Value: the protocol

Share the Value is an open specification that anyone can implement. It covers four things:

1. **Consent**: what a person agrees to share, with whom, and for how long.
2. **Matching**: how a platform reaches the right people without receiving their raw data.
3. **Attribution**: how a sale is linked to a consented match and verified.
4. **Payouts**: how the value of a verified sale is split.

### Principles

- **Coexist with existing platforms.** The platform keeps the majority share; the person receives a fraction.
- **Cash first.** Payouts are made in cash first, with credits as an option later.
- **Verified, unreturned sales only.** No payout is made on a sale that is not verified or that is returned.
- **Measured lift.** Lift is measured against a holdout group, so value is shown rather than assumed.
- **No disruption.** Existing ads continue as normal for people who do not opt in.

## 3. Pidlock: the person's vault

Pidlock keeps a person's PID (personally identifiable data) locked, and shares it only with consent.

- Data stays on the person's own device.
- Access can be switched on or off for each company at any time.
- Businesses never receive raw data.

## 4. Who benefits

These are expectations to be tested, not results.

- **Platforms** keep the majority share, can offer a consent-based option people may prefer, and keep their existing ads.
- **Merchants** pay only for verified, unreturned sales, with lift measured against a holdout group.
- **People** choose who sees what, keep their data on their device, and receive a fair share when it helps.

## 5. Pilot

The first step is a pilot with one challenger platform. The pilot will test, with real numbers and a holdout group, whether the protocol works well for platforms, merchants and people. Results will be shared openly.

## 6. Open questions

- The exact consent and vault format.
- How verified-sale attestation works across merchants.
- The holdout-lift measurement method.
- How the split between platform and person is set and published.

## 7. License

This paper and the specification are licensed under CC BY 4.0. Code is licensed under Apache 2.0.
