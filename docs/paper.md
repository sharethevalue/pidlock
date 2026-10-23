# Share the value: a consent and compensation layer for digital platforms

By Akbar Lalani

**v0.2 draft**

*A thesis for compensating people for the data, attention and intent they contribute, in coexistence with today's platforms, and a call for an open, community-governed protocol. Public draft white paper, v0.2, October 2026. Proposed license: CC BY 4.0.*

## 1. The thesis

Platforms such as search engines, social networks, marketplaces and app stores create real value: they distribute, rank and connect people with merchants, and many livelihoods depend on them. Much of that value is built on personal data, attention and intent that people contribute, as people exchange personal data for free services, typically without direct compensation. This paper does not propose replacing or competing with these platforms. It proposes an open consent and compensation layer they can adopt. In this paper, **the layer** means two things together: **Pidlock**, the person's vault, and **the protocol**, the open specification for consent, matching and payouts. With the layer, the person's data stays in Pidlock, is used only with revocable consent, and earns the person a defined share, with a minimum share set in the specification, when consented intent leads to a verified sale. It applies both when an AI agent shops on a person's behalf and when people browse, search or scroll on their own. Platforms keep distributing and keep the majority share; merchants reach people through consented intent; people are compensated for what they contribute. The aim is peaceful coexistence and a win-win for every party, to be tested: share the value, so nobody loses their livelihood.

## 1a. Benefits for every party (to be tested)

| Party | What it gets today | What it could get with the layer |
|---|---|---|
| **Platforms** | On feeds, display, video and connected TV, ad revenue rests largely on inferred signals, so intent is partly guesswork; growing legal attention to tracking. | Consented intent where they now infer it, plus context such as budget and timing; a design intended to align with consent and portability rules, subject to legal review[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html)[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025); a potential trust benefit (unmeasured); and the majority share of each payment (section 4b). |
| **Merchants** | Pay for clicks or impressions, some of which never convert; reputation held inside each channel. | Less wasted spend, payment per verified, unreturned sale at no more than today's cost per sale, and portable, signed reputation (W3C VC 2.0[[11]](https://www.w3.org/TR/vc-data-model-2.0/)). |
| **People** | Exchange personal data for free services, typically without direct compensation. | A user share paid out when their consented intent leads to a verified sale; control through Pidlock and scoped revocable keys; and offers matched to what they said they want. |

**The core argument for platforms: consented intent may be worth more than inferred intent, where intent is inferred today.**

- **Where the gain is.** On feeds, display, video and connected TV, platforms infer intent from behaviour. Consented intent replaces part of that guesswork with what the person says they want. Search gains less, because a query is already stated intent; even there, consented intent can add context a query lacks, such as budget, timing and constraints. Consented intent is *zero-party data* (data a person intentionally and proactively shares) and, once received by the platform, *first-party data* (data a business collects directly from its own users).
- **Overstated intent.** People may overstate interest to collect payouts. The protocol pays only on verified, unreturned sales, never for stating intent, and makes accuracy affect reach: a person whose consented intent rarely converts receives fewer offers.
- **Legal durability.** Signals based on explicit, revocable consent do not depend on third-party cookies or cross-site tracking, so they are less exposed as browsers and privacy laws restrict tracking. This is an argument, not a measured result.
- **Designed to align with consent and portability rules, subject to legal review.** Consent records that can be reviewed and withdrawn are designed to fit DPDP Consent Managers[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025)[[16]](https://sansad.in/getFile/lsapps/loksabhaquestions/annex/188/AU3943_458sox.pdf), DMA portability[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html) and GDPR consent requirements (section 7).
- **Potential trust benefit (unmeasured).** Paying people a user share for consented intent could improve trust; no measurement supports this yet.
- **Revenue kept.** The platform keeps the majority share of each payment; the user share is a fraction (section 4b).

> **Hypothesis, not fact.** That consented intent is more valuable than inferred intent is the authors' argument. It is the central hypothesis the holdout-tested pilot (section 8) is designed to test, by measuring incremental verified sales against conversion-optimised ads. A *holdout* is a randomly selected group that is not offered the payout, used as the comparison.

## 2. The problem: value is created from people's data, but not shared with them

- **Intent.** Search engines, social feeds, marketplaces and app stores are where people say or show what they want. That intent is highly valuable to merchants.
- **Data.** Clicks, conversions, returns, reviews and browsing history are generated by people and help platforms rank and target well.
- **Result.** People exchange personal data for free services, typically without direct compensation for the value their data and attention create. Consent is often broad and hard to review or withdraw.
- **The shift under way.** Agentic shopping is being standardised by major companies (ACP, UCP, AP2 and card network programs; see section 5). These standards cover checkout, payment and agent identity. They do not yet define how the person who supplies data, attention or intent is compensated. That is the gap the layer could fill, alongside these standards.

## 3. Principles

- **Consent first.** Personal data stays in Pidlock, the vault the person controls. It is used only under a scoped revocable key the person accepts, for a stated purpose.
- **Share the value.** When consented data or consented intent creates value, the person who contributed it receives a defined share, with a minimum share set in the specification, alongside the platform that distributed it.
- **Platforms keep their role.** Platforms continue to distribute, rank and earn the majority share. The layer is something they can adopt, not something built to replace them.
- **Portable trust.** Merchants can carry verified, purchase-tied outcome records, signed so they remain usable across channels.

## 4. The combined model: Pidlock and the protocol

Pidlock is the person's vault. The name comes from PID, personally identifiable data, which stays locked and is shared only with the person's consent. It is an encrypted store for personal data that the person controls. Platforms and merchants that adopt the protocol request access through a *scoped revocable key*, meaning a key limited to one party and one purpose that the person can withdraw at any time, after which access ends. The person accepts, declines or revokes, and consented use that leads to a verified sale is settled as a payout of the user share. **The person is paid for consented use of their data and consented intent, rather than providing it without compensation.**

> **What the original Pidlock concept said about money.** The original document does not set percentages. It describes three flows: (1) a person who chooses to share data with approved third parties is paid "for a small fee/month", priced "at fair value based on a user scoring system" by category, with ad platforms expected to be the main buyers; (2) for a sharing user the service is free, because it "will generate a small transactional fee when the user data is monetized"; (3) a person who blocks all sharing "pays a small service fee to support the platform". Its stated aim: users should be "rewarded for sharing" data that was "otherwise being used for FREE". This paper keeps the principles of a small transactional fee and payment to the person, and moves from bulk data sales to per-event payouts (see cautions below).

1. **Pidlock.** Data stays in the person's vault, by default on their device. Nothing is used without a scoped revocable key the person accepts.
2. **Consented intent.** The person, or their agent, states an intent, for example "running shoes, within a budget, delivered this week", as a signed message similar in spirit to an AP2 Intent Mandate.[[5]](https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol)
3. **Offers through platforms.** Platforms that adopt the protocol, and merchants on them, can respond to consented intent with offers. Platforms continue to distribute and rank as they do today.
4. **Platform keeps the majority share; the person gets a fraction.** When a merchant pays for a verified outcome from consented intent, the distributing platform keeps most of each payment, as it does today, for reach and ranking. The person receives the user share, a fraction paid for their attention or the outcome, not as a sale of data. Payouts start as cash through regulated payment partners. Credits that can be spent on subscriptions or withdrawn as cash may come later, through a gift-card partner, because stored-value and e-money rules apply to credits and vary by country. Any protocol fee is optional and small. A minimum user share is written into the conformance tests; its level is set by the community.
5. **Private matching.** Matching between consented intent and offers runs on the device or in *confidential compute* (hardware-isolated processing that even the operator cannot inspect), so merchants never receive raw personal data and revoking a key actually ends access.
6. **Outcome-informed ranking.** Verified outcomes such as receipts, return rates and repeat purchases can inform ranking. Platforms keep control of their own ranking; a *conformant integration* (one that passes the protocol's published conformance tests) discloses where paid placement applies.
7. **Portable reputation.** Each verified purchase yields a signed outcome credential (W3C VC 2.0[[11]](https://www.w3.org/TR/vc-data-model-2.0/)) that the merchant holds and can present anywhere.
8. **Contact only by key.** Name, phone or email are shared only when the person accepts a scoped revocable key for one merchant and purpose.
9. **Existing rails for checkout.** Purchases complete through ACP, UCP or AP2 where available. The protocol does not rebuild payments.

> **Cautions carried over from the original concept:** the design avoids bulk resale of data dumps, category grading of people for data pricing, and a bundled VPN. Individual data records have low resale value on their own, deleting data already copied to a third party cannot be technically enforced, and a VPN adds cost and friction without helping distribution. This is why the protocol favours scoped revocable keys and per-use consent and pays per real event, rather than handing over copies of data.

## 4a. Why platforms would adopt it

These are arguments for discussion, not claims of demonstrated demand.

- **Designed to align with consent and portability rules, subject to legal review.** India's DPDP Rules 2025 introduce registered Consent Managers through which people give, review and withdraw consent[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025)[[16]](https://sansad.in/getFile/lsapps/loksabhaquestions/annex/188/AU3943_458sox.pdf). The EU Digital Markets Act requires designated gatekeepers to support data portability for end users and authorised third parties[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html). A standard consent and compensation layer is designed to help platforms meet such obligations consistently, subject to legal review.
- **Better data where intent is inferred today.** Consented intent may be more accurate than inferred intent on feeds, display, video and connected TV, and adds context such as budget and timing to search. A hypothesis to test (section 1a).
- **Potential trust benefit (unmeasured).** Paying people a user share for consented use of their data could improve trust and willingness to share.
- **Continuity.** Platforms keep distribution, ranking and the majority share of revenue. Adoption adds a consented, compensated channel rather than replacing existing business.
- **Compatibility.** The protocol builds on standards platforms already back, such as ACP, UCP, AP2 and VC 2.0 (section 5).

**Adoption path.**

1. **Challenger agents and platforms** first, with a simple message to their users: "you're rewarded when your stated intent leads to a purchase". Large platforms already sell pay-per-sale, conversion-optimised ads and keep all of the spend (section 4b), so challengers have the clearest reason to differentiate.
2. **Merchants** who pay per verified sale rather than per click, so they pay only for outcomes.
3. **Regulators and compliance teams**, through a compliance kit that maps the protocol to DMA portability and DPDP consent flows[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html)[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025).
4. **Large platforms** join when a clear trigger appears. The lead bet: advertisers demanding verified, consented inventory. Alternatives: regulation that requires consent records, or challengers gaining measurable share with consented intent.

## 4b. Economic model: three scenarios

Three internally consistent scenarios test whether the platform can keep the majority share, the person can receive a fraction, and the merchant can be no worse off. They are illustrations, not any real merchant's numbers.

**The right baseline.** Large platforms already sell conversion-optimised products, such as Google Ads target CPA (bidding toward a target cost per acquisition) and target ROAS (bidding toward a target return on ad spend) and Meta conversion campaigns, in which advertisers bid toward a cost per sale and the platform keeps 100% of the ad spend. The comparison is therefore against those products, not against plain search clicks. Paying per sale alone is not new; what is new is consented intent and the user share. For this reason challenger agents and platforms, which do not yet have such products at scale, are the natural first adopters.

**How each scenario works.** The merchant pays the same cost per sale as its current conversion-optimised campaign (so it is no worse off), but only on a verified, unreturned sale. The platform keeps the majority share, the person receives the user share and an optional 1% goes to the protocol. The platform matches today's revenue only if the layer produces more incremental sales for the same audience: required lift = 1 / (platform share) minus 1. Lift is measured as incremental lift against a holdout group that is not offered the payout, not as raw conversion.

| Per sale | A. High-margin DTC brand (apparel) | B. Marketplace seller (general retail) | C. Subscription app |
|---|---|---|---|
| Order or first-year revenue | $150 (ECDB 2025 worldwide gross AOV[[22]](https://ecdb.com/resources/sample-data/market/ww/all/transactions)) | $150 (ECDB[[22]](https://ecdb.com/resources/sample-data/market/ww/all/transactions)) | $60, i.e. $5 a month for 12 months (**assumption**) |
| Gross margin | 56.88%, Apparel (Damodaran, Jan 2026[[23]](https://pages.stern.nyu.edu/adamodar/New_Home_Page/datafile/margin.html)) | 33.18%, Retail (General)[[23]](https://pages.stern.nyu.edu/adamodar/New_Home_Page/datafile/margin.html) | 71.72%, Software (System and Application)[[23]](https://pages.stern.nyu.edu/adamodar/New_Home_Page/datafile/margin.html) |
| Gross profit | $85.32 | $49.77 | $43.03 |
| Current cost per sale on conversion-optimised ads | $40 (**assumption**) | $20 (**assumption**; marketplace commission not modelled) | $25 (**assumption**) |
| Merchant gross profit after ads today | $45.32 (positive) | $29.77 (positive) | $18.03 (positive) |
| User share (**assumption**) | 15%: $6.00 | 5%: $1.00 | 20%: $5.00 |
| Protocol fee, 1% (**assumption**) | $0.40 | $0.20 | $0.25 |
| Platform keeps | $33.60 (84%) | $18.80 (94%) | $19.75 (79%) |
| Merchant cost per sale | $40 (unchanged) | $20 (unchanged) | $25 (unchanged) |
| **Required incremental lift vs conversion-optimised ads** | **about 19.0%** | **about 6.4%** | **about 26.6%** |

Revenue and margin inputs are cited where a benchmark exists; costs per sale, user shares and the subscription price are assumptions chosen so that no scenario loses money per sale today. Gross margin excludes fulfilment, returns and other operating costs. Reference search benchmarks for context: average Google Ads cost per click $5.26 and conversion rate 7.52% across industries, US, April 2024 to March 2025 (WordStream[[21]](https://www.wordstream.com/blog/2025-google-ads-benchmarks)).

**Hypothesis to prove first:** for the same audience, consented intent with a user share produces at least the lift above (about 6% to 27% across these scenarios) in incremental verified sales over the platform's own conversion-optimised campaigns, measured with holdouts. No source supports this yet; it is what the first pilot must test.

## 4c. Scope: agents and self-browsing

The layer covers two situations with the same building blocks: Pidlock, scoped revocable keys, payouts on verified outcomes, and on-device matching.

- **Agent-assisted shopping.** A person's AI agent expresses consented intent and completes checkout, for example through ACP, UCP or AP2[[2]](https://docs.stripe.com/agentic-commerce/protocols/acp)[[4]](https://developers.googleblog.com/en/under-the-hood-universal-commerce-protocol-ucp/)[[5]](https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol). This is the easiest place to start, because intent is already explicit and structured.
- **Self-browsing.** People searching, browsing or scrolling on their own take part mainly through an opt-in on the platform's own surfaces or an in-app or operating-system-level consent setting. Consented intent is formed on the device from what the person chooses to share, and nothing leaves the device without a scoped revocable key.
- **Browser extension (secondary route).** An extension is display-only and fully disclosed: it shows offers matched to consented intent and the user share on offer, and never adds, removes or replaces affiliate links, codes or cookies, so it never touches affiliate attribution. Affiliate-link swapping by shopping extensions has drawn public criticism, notably the 2024 to 2025 controversy over PayPal's Honey[[25]](https://www.theverge.com/news/627940/google-chrome-extensions-paypal-honey-affiliate), and the Chrome Web Store tightened its affiliate ads policy in March 2025, with enforcement from 10 June 2025[[24]](https://developer.chrome.com/blog/cws-policy-update-affiliate-ads-2025).

## 4d. Impact on advertising and remarketing

**What stays the same.** Existing search, social and display ads keep running unchanged. People who do not opt in see no change, so nothing is taken away from platforms' current advertising business.

**What changes.**

- **A new opt-in placement type.** A person who opts in expresses consented intent, sees relevant offers, and receives the user share when a verified sale happens. It sits alongside existing ad formats as one more campaign type.
- **Consented remarketing (optional add-on).** People can opt in to reminders, for example about products they viewed, and receive a payout if they buy. Merchants already reach past visitors cheaply through first-party email and abandoned-cart flows, so value is claimed only for new or cross-merchant reach, such as reminders about similar products from other sellers, and only where holdout tests show incremental sales. Because it rests on explicit consent held in Pidlock rather than on cross-site tracking, the authors argue it could keep working as browser privacy changes and privacy laws limit tracking-based remarketing. This is an argument, not a measured result.
- **Measurement.** Payouts are made on verified, unreturned sales, which gives a direct attribution record rather than a modelled or estimated conversion.

**The risk, stated plainly.** Platforms may worry that a consented, paid placement becomes a template that regulators later use to require consent for all ads. The authors' view is that this direction is already visible in rules such as the DMA and DPDP[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html)[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025), and that platforms which pilot consented formats early gain experience, tooling and the potential trust benefit ahead of any such requirement. This is an argument, not a prediction.

**Transition path for a platform.**

1. **Pilot:** launch as one opt-in campaign type, in one market or category, alongside existing ads.
2. **Reporting:** publish results to advertisers on verified sales, returns, payouts and holdout-measured incremental lift compared with existing campaigns (the hypothesis in section 4b).
3. **Wider rollout:** extend to more categories, consented remarketing and self-browsing surfaces if the results hold.

## 5. What already exists and where the gap is

| Effort | What it covers | Status | Gap for this thesis |
|---|---|---|---|
| **Agentic Commerce Protocol (ACP)**[[1]](https://openai.com/index/buy-it-in-chatgpt/)[[2]](https://docs.stripe.com/agentic-commerce/protocols/acp)[[3]](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol) | Checkout sessions, delegated payment, cart and feed, order webhooks between agent and merchant. Maintained by OpenAI and Stripe; Stripe docs also name Meta as a creator. | Open spec, Apache 2.0, beta. Powers ChatGPT Instant Checkout; merchants pay a fee on completed purchases. | Ranking stays inside the host agent. No consented intent with a user share, no portable reputation. |
| **Universal Commerce Protocol (UCP)**[[4]](https://developers.googleblog.com/en/under-the-hood-universal-commerce-protocol-ucp/) | Discovery, checkout and post-purchase across agents. Co-developed by Google with Shopify, Etsy, Wayfair, Target, Walmart; works with AP2, A2A, MCP. | Open source. First surface: Google AI Mode and Gemini. | Ranking and advertising economics remain with the host surface. |
| **Agent Payments Protocol (AP2)**[[5]](https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol) | Signed Intent and Cart Mandates backed by verifiable credentials prove what a user authorised. | Open protocol, 60+ launch collaborators. Payment-agnostic. | The Intent Mandate is a strong primitive, but no market lets merchants reach that intent with consent and pay the person. |
| **Visa Trusted Agent Protocol, Mastercard Agent Pay**[[6]](https://corporate.visa.com/en/sites/visa-perspectives/newsroom/visa-unveils-trusted-agent-protocol-for-ai-commerce.html)[[7]](https://blog.cloudflare.com/secure-agentic-commerce/)[[8]](https://www.mastercard.com/global/en/business/artificial-intelligence/mastercard-agent-pay.html) | Registered agents sign requests (Web Bot Auth, HTTP Message Signatures); tokenised agent credentials. | Visa spec open source; agent directories hosted by each network. | Trust sits with the agent and card network, not with the person or the seller's reputation. |
| **Shopify Agentic Storefronts, Catalog MCP**[[9]](https://www.shopify.com/blog/how-agentic-commerce-works)[[10]](https://shopify.dev/changelog/posts/storefront-catalog-mcp-now-implements-ucp) | Exposes merchant catalogs to ChatGPT, Copilot, Google AI Mode and Gemini; catalog MCP implements UCP. | Live for eligible merchants. | Reach still depends on each host's ranking. |
| **W3C Verifiable Credentials 2.0**[[11]](https://www.w3.org/TR/vc-data-model-2.0/) | Standard model for signed, tamper-evident claims with privacy features such as selective disclosure. | W3C Recommendation, 15 May 2025. | A building block. The authors are not aware of a widely used commerce-reputation schema built on it (unverified). |
| **World ID (proof of personhood)**[[12]](https://world.org/blog/announcements/world-id-full-stack-proof-of-human) | Anonymous one-human-per-account credential issued after an Orb scan. | Live. Biometric and centralisation concerns are publicly debated. | Could limit payout farming, but depends on one operator and special hardware. |
| **EU Digital Markets Act, Art. 6(9)**[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html)[[14]](https://developers.google.com/data-portability/user-guide/introduction) | Gatekeepers (as designated under the DMA) must let end users and authorised third parties port data free of charge, continuously and in real time. | In force. Google offers a Data Portability API to approved apps. | Lets Pidlock import history in the EU; does not touch ranking or attention. |
| **India DPDP Rules 2025, Consent Managers**[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025)[[16]](https://sansad.in/getFile/lsapps/loksabhaquestions/annex/188/AU3943_458sox.pdf) | Registered Consent Managers let people give, review and withdraw consent through interoperable platforms. | Rules notified 13 Nov 2025; Consent Manager rule effective 13 Nov 2026; core duties from 13 May 2027. | A legal rail for consent records; silent on paying people. |

**The gap.** Rails for agent checkout, payment authorisation, agent identity and consent are being built, largely in the open, by major companies. What none of them defines is how the person who contributes data, attention or intent shares in the value it creates. A shared, open consent and compensation layer, which platforms can plug into alongside these standards, could fill that gap without changing who distributes.

**The closest existing competitor: cashback, affiliate and rewards programs.** Cashback portals such as Rakuten, coupon and cashback extensions such as Honey, and card rewards programs already pay people when they buy. The layer differs in four ways: (1) the person's data stays in Pidlock and is matched on device, instead of being collected by the rewards operator; (2) consent is explicit and given through scoped revocable keys; (3) it works with consented intent before a purchase, including through agents, not only on clicks through to a checkout; and (4) it does not alter affiliate attribution. Whether these differences matter enough to people and merchants is part of what the pilot must test.

## 6. Why past attempts failed and how this differs

| Attempt | What happened | How this model differs |
|---|---|---|
| **Datacoup (closed Nov 2019)**[[17]](https://www.reddit.com/r/beermoney/comments/dyvxj4/datacoup_closing/) | Its closing notice stated that user data was never sold and past payments came from its treasury. | Payouts come from consented use through platforms that already earn from data and intent, not from a separate data marketplace. |
| **Gener8**[[18]](https://tech.eu/2023/03/15/gener8-expands-the-future-of-data/) | Reported UK users earning about £5 to £25 a month in rewards points (2023). One user review describes a hard-to-use rewards store and no cash out (anecdotal). | Settle in ordinary money, triggered by real events, not points. |
| **Brave BAT**[[19]](https://snat.co.uk/reviews/money/brave-browser-or-gener8-browser.html) | Pays a token for opted-in ad views. User reports describe small or delayed payouts and KYC friction (anecdotal; no aggregate data verified). | Pay on verified sales from consented intent, in ordinary money. |
| **Swash / Streamr Data Unions**[[20]](https://blog.streamr.network/an-update-on-data-unions-and-first-look-at-rail-on-chain-group-payments-for-web3/) | Streamr paused Data Union DAO fundraising, stating the business case was not strong enough to attract venture capital. | Price consented intent and outcomes, not bulk browsing data. |

The common thread: these projects tried to build separate markets for passive data or views, paid in points or tokens, and needed buyers who had cheaper options. This model works with the platforms where value is already created, shares that value with the person per real event in ordinary money, and builds on agent checkout standards now going live.

## 7. Risks and open questions

- **Platform adoption.** The layer depends on platforms choosing to integrate. A plausible start is one challenger platform or agent piloting consented intent with a user share in one region. Unproven.
- **Fraud and proof of personhood.** Payouts invite fake accounts and overstated intent. Proposed defences: pay only on verified, unreturned outcomes; layered personhood checks (payment instrument, device attestation, optional verifiable credentials or proof of personhood[[12]](https://world.org/blog/announcements/world-id-full-stack-proof-of-human)); hold payouts until the return window closes; reduce reach for people whose consented intent rarely converts; and reputation staking, where repeat bad actors lose a stake. Not yet proven in practice.
- **Setting the split.** Setting the user share, platform share and any protocol fee so that all three find it worthwhile is unresolved and needs open discussion and testing.
- **Transparency.** People need to see what was shared, with whom, and what payouts they received. Needs auditable records and conformance tests.
- **Protocol sustainability.** Who funds maintenance: a foundation, sponsors, or a minimal protocol fee? Open.
- **Integration cost.** Platforms differ in architecture and policy. The protocol must be simple to integrate; OpenAI, for example, states ChatGPT product results are organic and unsponsored today[[1]](https://openai.com/index/buy-it-in-chatgpt/), so each host would decide how, and whether, offers on consented intent fit.
- **Legal.** Payouts are framed as payment for attention or an outcome, not a sale of data. Under the GDPR, consent must be freely given, and the EDPB has said that in most cases large online platforms cannot obtain valid consent by offering only a binary choice between consenting to behavioural advertising and paying a fee[[26]](https://www.edpb.europa.eu/system/files/2024-04/edpb_opinion_202408_consentorpay_en.pdf). In April 2025 the European Commission found Meta's "consent or pay" model in breach of the DMA and fined it 200 million euros[[27]](https://ec.europa.eu/commission/presscorner/api/files/document/print/en/ip_25_1085/IP_25_1085_EN.pdf). A payout must therefore not pressure people into consenting: declining must leave the service unchanged, and consent must stay specific and revocable. Data stays on the device, with local or confidential-compute matching, so merchants never receive raw data and revocation is real. Payouts settle through regulated payment partners that handle KYC and tax. Consumer protection, payments and tax law vary by country, so a legal opinion is needed per jurisdiction before launch.
- **Standards alignment.** UCP, ACP and AP2 are being adopted in 2026[[4]](https://developers.googleblog.com/en/under-the-hood-universal-commerce-protocol-ucp/)[[9]](https://www.shopify.com/blog/how-agentic-commerce-works). The protocol should be designed to complement them, so integration stays straightforward. This is the authors' assessment, not a forecast.

## 8. The cheapest global proof and success signals

A protocol, not an app. Within 60 days:

1. Publish an open draft spec covering consented intent, offer, sale settlement and payout, outcome credential and contact key, reusing AP2 mandates and ACP or UCP checkout where possible.
2. Ship a reference MCP plugin so any agent can send consented intent and receive ranked offers, plus a minimal seller-side responder.
3. **Next step:** a holdout-tested pilot with one challenger agent that funds the user share out of its own margin. Its users are randomly split so that a holdout group is not offered the payout, and the pilot measures incremental verified, unreturned sales against the same merchants' conversion-optimised ads (section 4b).

**Signals** (thresholds to be agreed openly; none are benchmarks): independent agent builders integrating without outreach; sellers publishing offers and accepting per-sale pricing in principle; outside issues, pull requests and forks; at least one real purchase completed with a verified outcome credential; engagement from existing protocol communities.

## 9. Open design decisions

1. Minimum user share, payout forms (cash first; credits through a gift-card partner later, subject to stored-value and e-money rules), and the size of any optional protocol fee. The platform keeps the majority share.
2. Future option: whether credits spent on subscriptions to other tools and services could benefit the wider ecosystem. Not claimed; to be evaluated later.
3. First fraud defence to test: payout on verified sale only, proof of personhood, or payment-rail identity.
4. Which existing standards to bind to first (AP2 mandates, ACP, UCP, VC 2.0).
5. Outcome credential schema: which signals count, and who may issue them.
6. Numeric thresholds for the 60-day signals.
7. Whether and how to hold a trademark on the protocol name, and which neutral foundation or standards body should host the protocol.

## 10. Proposed open spec and licensing

- **This paper:** Creative Commons Attribution 4.0 (CC BY 4.0).
- **Specification text and schemas:** CC BY 4.0, or W3C Community Group or IETF terms if hosted there, with a royalty-free patent commitment from contributors.
- **Reference implementation and MCP plugin:** Apache 2.0, which includes an explicit patent grant and matches ACP's license[[3]](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol).
- **Spec shape:** versioned message schemas (JSON Schema, OpenAPI), a conformance test suite including the minimum user share, and short normative rules on consent, revocation, disclosure of paid placement and payout of the user share.
- **Name:** the protocol name held by a neutral body, usable by any conformant integration (trademark approach still an open decision, section 9).

## 11. Call to the community

This is meant to be an open protocol developed and governed by its community, not a company product, so that people, platforms and merchants can all trust the rules for consent and value sharing.

**How to contribute**

- A public GitHub repository holding the spec, schemas, reference code and this paper.
- An RFC process: anyone opens a numbered proposal as a pull request, discussion runs in public for a fixed comment period, and maintainers record the decision and reasons.
- Issues labelled "good first problem" for newcomers; a public meeting cadence with published notes.

**Open problems to pick up first**

1. Consented intent message schema and its mapping to AP2 Intent Mandates.
2. Platform integration guide and SDK: how a platform requests consent, shows offers on consented intent and reports settlement.
3. Payout of the user share (cash first, credits later) through regulated payment partners, with return-window holdbacks, resistant to click and view farming.
4. Compliance kit mapping the protocol to DMA portability, DPDP consent and GDPR consent requirements.
5. Reference browser extension for self-browsing: Pidlock connection, consent prompts, on-device matching, and opt-in consented remarketing reminders with a payout on purchase.
6. Pidlock design: key scoping, revocation and per-use payout records.
7. Outcome credential schema on VC 2.0, with selective disclosure.
8. Privacy-preserving proof of personhood options and their trade-offs.
9. Reference MCP plugin and a minimal seller responder.
10. Conformance tests for consent, the minimum user share, disclosure of paid placement and payout to the person.
11. Mapping consent records to DPDP Consent Managers and DMA portability flows[[13]](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html)[[15]](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025).

**Lightweight, neutral governance**

- Start with a small maintainer group drawn from several organisations, with a cap on seats from any one organisation.
- Decisions by rough consensus in public; contested items go to a recorded maintainer vote.
- A written code of conduct and conflict-of-interest disclosure.
- Once there is real adoption, move the protocol to a neutral foundation or standards body, with vote caps per organisation and dedicated seats for people and merchants. Which body is an open decision (section 9).
- The minimum user share and the consent rules are written into the conformance tests, so only implementations that pay people and honour consent pass.

## 12. Conclusion

People already contribute the data, attention and intent that power today's platforms, typically without direct compensation. This paper proposes sharing that value rather than contesting who distributes it: an open consent and compensation layer, made of Pidlock and the protocol, that platforms can adopt, in which the person receives a defined share for consented use, the platform keeps the majority share for distribution, and the rules are set openly by the community. The goal is coexistence in which nobody loses their livelihood and everyone who creates value receives a defined share of it.

## References

1. [OpenAI, "Buy it in ChatGPT: Instant Checkout and the Agentic Commerce Protocol" (2025)](https://openai.com/index/buy-it-in-chatgpt/)
2. [Stripe Docs, "Agentic Commerce Protocol"](https://docs.stripe.com/agentic-commerce/protocols/acp)
3. [ACP specification repository (GitHub)](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol)
4. [Google Developers Blog, "Under the Hood: Universal Commerce Protocol (UCP)" (11 Jan 2026)](https://developers.googleblog.com/en/under-the-hood-universal-commerce-protocol-ucp/)
5. [Google Cloud Blog, "Announcing Agent Payments Protocol (AP2)" (16 Sep 2025)](https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol)
6. [Visa, "Visa Introduces Trusted Agent Protocol" (14 Oct 2025)](https://corporate.visa.com/en/sites/visa-perspectives/newsroom/visa-unveils-trusted-agent-protocol-for-ai-commerce.html)
7. [Cloudflare Blog, "Securing agentic commerce: helping AI Agents transact with Visa and Mastercard"](https://blog.cloudflare.com/secure-agentic-commerce/)
8. [Mastercard, "Mastercard Agent Pay"](https://www.mastercard.com/global/en/business/artificial-intelligence/mastercard-agent-pay.html)
9. [Shopify, "Agentic Commerce on Shopify: How It Works" (2026)](https://www.shopify.com/blog/how-agentic-commerce-works)
10. [Shopify Dev Changelog, "Storefront Catalog MCP now implements UCP"](https://shopify.dev/changelog/posts/storefront-catalog-mcp-now-implements-ucp)
11. [W3C, "Verifiable Credentials Data Model v2.0", Recommendation (15 May 2025)](https://www.w3.org/TR/vc-data-model-2.0/)
12. [World, "World ID Full-Stack Proof of Human"](https://world.org/blog/announcements/world-id-full-stack-proof-of-human)
13. [Digital Markets Act, Article 6 (text)](https://www.eu-digital-markets-act.com/Digital_Markets_Act_Article_6.html)
14. [Google for Developers, "Data Portability API"](https://developers.google.com/data-portability/user-guide/introduction)
15. [Legal 500, "Notification of the Digital Personal Data Protection Rules, 2025"](https://www.legal500.com/intelligence/india/privacy/regulatory-update-notification-of-the-digital-personal-data-protection-rules-2025)
16. [MeitY, Lok Sabha Unstarred Question No. 3943 (12 Aug 2026)](https://sansad.in/getFile/lsapps/loksabhaquestions/annex/188/AU3943_458sox.pdf)
17. [Datacoup closing notice, as posted on r/beermoney (Nov 2019)](https://www.reddit.com/r/beermoney/comments/dyvxj4/datacoup_closing/)
18. [Tech.eu, "Gener8's new app..." (15 Mar 2023)](https://tech.eu/2023/03/15/gener8-expands-the-future-of-data/)
19. [Tales of Snat, "Brave Browser or Gener8 Browser" (user review)](https://snat.co.uk/reviews/money/brave-browser-or-gener8-browser.html)
20. [Streamr Blog, "An update on Data Unions and first look at Rail"](https://blog.streamr.network/an-update-on-data-unions-and-first-look-at-rail-on-chain-group-payments-for-web3/)
21. [WordStream, "Google Ads Benchmarks 2025" (16,000+ US campaigns, Apr 2024 to Mar 2025)](https://www.wordstream.com/blog/2025-google-ads-benchmarks)
22. [ECDB, "E-Commerce Conversion Funnel Benchmarks Worldwide" (2025 average order value)](https://ecdb.com/resources/sample-data/market/ww/all/transactions)
23. [A. Damodaran, NYU Stern, "Margins by Sector (US)" (data as of Jan 2026)](https://pages.stern.nyu.edu/adamodar/New_Home_Page/datafile/margin.html)
24. [Chrome for Developers, "Chrome Web Store policy updates: Strengthening our policies on affiliate programs in Chrome Extensions" (11 Mar 2025)](https://developer.chrome.com/blog/cws-policy-update-affiliate-ads-2025)
25. [The Verge, "Google changes Chrome extension policies following the Honey link scandal" (12 Mar 2025)](https://www.theverge.com/news/627940/google-chrome-extensions-paypal-honey-affiliate)
26. [EDPB, "Opinion 08/2024 on Valid Consent in the Context of Consent or Pay Models Implemented by Large Online Platforms" (17 Apr 2024)](https://www.edpb.europa.eu/system/files/2024-04/edpb_opinion_202408_consentorpay_en.pdf)
27. [European Commission, "Commission finds Apple and Meta in breach of the Digital Markets Act", press release IP/25/1085 (23 Apr 2025)](https://ec.europa.eu/commission/presscorner/api/files/document/print/en/ip_25_1085/IP_25_1085_EN.pdf)

> **Verification notes (v0.2).** Facts are cited to their sources, accessed October 2026. Items marked anecdotal rest on single user reports. Statements about gaps, adoption incentives and platform behaviour are the authors' analysis. Figures marked as assumptions are illustrative and not sourced.
