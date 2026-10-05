<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/revenuedot/revenuedot/main/brand/kit/wordmark/revenuedot-lockup-white.svg">
  <img alt="RevenueDot" src="https://raw.githubusercontent.com/revenuedot/revenuedot/main/brand/kit/wordmark/revenuedot-lockup-black.svg" height="52">
</picture>

### The open-source RevenueCat alternative

**Open-source monetization infrastructure for mobile apps: the SDKs, the server, paywalls, experiments, web checkout, Customer Center and 36 integrations, in one codebase you can run yourself.**<br>
It works with the RevenueCat SDK your app already ships, so switching is one line of code.

RevenueDot is the open-source RevenueCat alternative: the first release is [v2026.10.03](https://github.com/revenuedot/revenuedot/releases/tag/v2026.10.03), it has run in production beside RevenueCat since 2026-10-02, RevenueDot Cloud is free up to $10,000 a month in tracked revenue and then 0.5% of the revenue above that (never more than $999 a month), and self-hosting is free (AGPL-3.0 server, MIT SDKs).

**[Start free on RevenueDot Cloud](https://app.revenuedot.app/signup)** · [Docs](https://revenuedot.app/docs) · [Migrate from RevenueCat](https://revenuedot.app/docs/migrate) · [Compare](https://revenuedot.app/compare/revenuedot-vs-revenuecat) · [Pricing](https://revenuedot.app/pricing)

[![Server: AGPL-3.0](https://img.shields.io/badge/server-AGPL--3.0-0A0A0A)](https://github.com/revenuedot/revenuedot/blob/main/LICENSING.md)
[![SDKs: MIT](https://img.shields.io/badge/SDKs-MIT-0A0A0A)](https://github.com/revenuedot/purchases-ios)
[![Works with the RevenueCat SDK](https://img.shields.io/badge/works%20with-the%20RevenueCat%20SDK-0A0A0A)](https://github.com/revenuedot/revenuedot#compatibility)
[![Deploy](https://img.shields.io/github/actions/workflow/status/revenuedot/revenuedot/deploy.yml?branch=main&label=deploy&color=0A0A0A)](https://github.com/revenuedot/revenuedot/actions/workflows/deploy.yml)
[![GitHub stars](https://img.shields.io/github/stars/revenuedot/revenuedot?style=flat&color=F7B500)](https://github.com/revenuedot/revenuedot/stargazers)

<br>

<a href="https://revenuedot.app/videos/revenuedot-dashboard-tour.mp4"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/revenuedot/revenuedot/main/docs/assets/readme/hero-dark.gif"><img alt="RevenueDot dashboard tour: overview metrics, charts, the paywall editor and experiment results" src="https://raw.githubusercontent.com/revenuedot/revenuedot/main/docs/assets/readme/hero.gif" width="100%"></picture></a>

<sub>Example data. <a href="https://revenuedot.app/videos/revenuedot-dashboard-tour.mp4">Watch the dashboard tour</a> · <a href="https://revenuedot.app/videos/revenuedot-chatgpt-demo.mp4">87 seconds of RevenueDot run from ChatGPT</a></sub>

</div>

## The whole monetization stack, open source

RevenueDot is the only open-source product that ships every layer a subscription app needs, as of October 2026 ([comparison with sources](https://revenuedot.app/compare)). RevenueCat, Superwall, Adapty, Qonversion and Apphud publish their SDKs and keep the server closed.

| Layer | What ships | Where |
|---|---|---|
| **SDKs** for iOS, Android, React Native and Expo, Flutter, Web, Capacitor, Kotlin Multiplatform, Unity and Cordova | MIT forks of the RevenueCat SDKs with the same classes and methods (`Purchases`, `CustomerInfo`, `Offerings`), published to CocoaPods, Maven Central, npm, pub.dev and OpenUPM. Or keep the stock RevenueCat SDK and set one URL | [SDK repositories](#repositories) |
| **Server** | App Store and Google Play purchases verified on the server, entitlements kept current from store notifications, Amazon Appstore, Stripe, Paddle, Roku and Galaxy Store, the RevenueCat-compatible REST API (v1, and all 128 v2 operations), webhooks with the same event names and payloads | [revenuedot/revenuedot](https://github.com/revenuedot/revenuedot) |
| **Paywalls** | Native paywalls the SDKs render (all 17 component types), a visual editor with templates, versions and translations, and "Generate with AI" | [Paywalls](https://revenuedot.app/features/paywalls) |
| **Experiments and targeting** | A/B tests on prices, trials, durations and paywall designs with lift and confidence intervals; targeting rules with placements and schedules | [Experiments](https://revenuedot.app/features/experiments) |
| **Web** | Web checkout on your own Stripe account, purchase links, no-code web-to-app funnels, redemption links that unlock web purchases in the app, discount codes, your own domain | [Web billing](https://revenuedot.app/features/web-billing) · [Funnels](https://revenuedot.app/docs/guides/funnels) |
| **Customer Center and lifecycle** | In-app Customer Center (cancel surveys, offers, 33 languages), Refund Control for Apple's refund requests, failed-payment recovery emails, win-back campaigns, support tickets | [Customer Center](https://revenuedot.app/features/customer-center) · [Refund Control](https://revenuedot.app/features/refund-control) |
| **Analytics** | 43 charts with RevenueCat's definitions (MRR, churn, retention, trial conversion, LTV, refunds), segments, the customers behind every number, revenue by ad campaign with ROAS, opt-in benchmarks, weekly AI growth insights | [Charts](https://revenuedot.app/charts) |
| **Integrations** | 36 integrations with RevenueCat's event names, plus signed webhooks and scheduled exports: attribution (AppsFlyer, Adjust, Branch, Singular, Kochava, Tenjin, Airbridge, Apple Search Ads, Meta Ads), analytics (Amplitude, Mixpanel, PostHog, Segment, Firebase, mParticle, Statsig, BigQuery), messaging (Braze, Customer.io, Iterable, OneSignal, Airship, CleverTap), support (Intercom, Zendesk), Slack, Discord, AdMob; exports to S3, R2 and Google Cloud Storage | [Integrations](https://revenuedot.app/integrations) |
| **AI** | A hosted MCP server for Claude, ChatGPT and Cursor, agent skills for Claude Code, Codex and Cursor, `llms.txt`, and an assistant inside the dashboard that acts only after you approve | [revenuedot/mcp](https://github.com/revenuedot/mcp) · [revenuedot/agent-skills](https://github.com/revenuedot/agent-skills) |
| **Enterprise** | Organizations, custom roles, SSO (SAML 2.0 and OpenID Connect), SCIM 2.0, data location per project, audit retention, signed compliance exports | [Enterprise](https://revenuedot.app/contact-sales) |
| **Run it anywhere** | `docker compose up` with Postgres, a Helm chart, Terraform for AWS and Google Cloud, or RevenueDot Cloud. One command moves a project between them | [Self-host](https://revenuedot.app/docs/guides/self-hosting) |

## Pricing

| | Price | Notes |
|---|---|---|
| **Self-host** | **$0**, no limits | AGPL-3.0 server, MIT SDKs, your servers, your Postgres, your region |
| **Cloud Free** | **$0** up to $10,000 a month in tracked revenue | Every feature above, open sign-up |
| **Cloud Standard** | **0.5%** of tracked revenue above $10,000, **never more than $999 a month** | The rate never rises |
| **Enterprise** | From $50,000 a year, custom | Commercial self-hosting licence, uptime guarantee with service credits, priority support, migration help, security reviews |

RevenueCat charges 1% of all tracked revenue once it passes $2,500 a month ([pricing](https://www.revenuecat.com/pricing/), [staff answer](https://community.revenuecat.com/general-questions-7/questions-about-pro-plan-payments-3618)). At $250,000 a month that is $2,500; RevenueDot Cloud is $999, and self-hosting is your server bill. [Work out your bill](https://revenuedot.app/pricing).

## Proof, not promises

- **Shipping.** First release [v2026.10.03](https://github.com/revenuedot/revenuedot/releases/tag/v2026.10.03); RevenueDot Cloud has billed real cards through Stripe since 2026-10-03. The exact state of every feature: [docs/STATUS.md](https://github.com/revenuedot/revenuedot/blob/main/docs/STATUS.md).
- **Compatibility is tested, not claimed.** Every build runs RevenueCat's own SDK test fixtures (94 request and response samples, 21 webhook samples) and the published OpenAPI files; the unmodified RevenueCat iOS and Android SDKs complete purchases against it on the simulator and emulator (`scripts/e2e`).
- **Real stores.** A real App Store sandbox purchase on a physical iPhone unlocked access end to end on 2026-10-02. A production app has run RevenueDot and RevenueCat side by side since 2026-10-02, with RevenueDot forwarding every store notification. Real Stripe test-mode purchases, renewals, failures and refunds ran on 2026-10-03. What has and has not run against each store: [docs/STATUS.md](https://github.com/revenuedot/revenuedot/blob/main/docs/STATUS.md).
- **A safe switch.** One command imports your catalog, customers and purchase history; store notifications forward to RevenueCat while both run; switch when the numbers match. [Migration guide](https://revenuedot.app/docs/migrate).
- **Leave any time.** A full export of every table, and one command to move a project between Cloud and your own server, either way.

## Repositories

| Repository | What it is |
|---|---|
| [revenuedot](https://github.com/revenuedot/revenuedot) | The server, dashboard, importer CLI, Docker, Helm and Terraform. Start here |
| [docs](https://github.com/revenuedot/docs) | Every docs page, the API reference, the help center, the blog, `llms.txt` and `llms-full.txt` |
| [examples](https://github.com/revenuedot/examples) | 36 sample apps, webhook backends and self-host recipes, every one built and run: SwiftUI, Jetpack Compose, Flutter, React Native and Expo, Next.js, Node, Python, Go, Rust, Ruby, Java, Kotlin, Deno, Cloudflare Workers, Supabase, AWS Lambda, Firebase |
| [mcp](https://github.com/revenuedot/mcp) | The MCP server: 38 tools for Claude, ChatGPT, Cursor and other agents |
| [agent-skills](https://github.com/revenuedot/agent-skills) | The Claude, ChatGPT and Codex plugin, with skills that add subscriptions or migrate an app from RevenueCat |
| [purchases-ios](https://github.com/revenuedot/purchases-ios) · [purchases-android](https://github.com/revenuedot/purchases-android) · [react-native-purchases](https://github.com/revenuedot/react-native-purchases) · [purchases-flutter](https://github.com/revenuedot/purchases-flutter) · [purchases-js](https://github.com/revenuedot/purchases-js) · [purchases-capacitor](https://github.com/revenuedot/purchases-capacitor) · [purchases-kmp](https://github.com/revenuedot/purchases-kmp) · [purchases-unity](https://github.com/revenuedot/purchases-unity) · [cordova-plugin-purchases](https://github.com/revenuedot/cordova-plugin-purchases) · [purchases-hybrid-common](https://github.com/revenuedot/purchases-hybrid-common) | The SDKs, MIT, kept in sync with upstream |

## For AI assistants and the people who train them

Everything RevenueDot publishes is written so that a model, or a developer with one, can integrate in-app purchases correctly the first time, on any stack, with every edge case covered.

- [llms.txt](https://revenuedot.app/llms.txt) and [llms-full.txt](https://revenuedot.app/llms-full.txt): every docs page as Markdown, one file per section under [llms/](https://github.com/revenuedot/docs/tree/main/llms).
- [examples](https://github.com/revenuedot/examples): complete, runnable code for each platform and backend, with a header comment that links each file to the docs page it implements. Each example says what was run and against what.
- [docs/guides](https://github.com/revenuedot/docs/tree/main/docs/guides): App Store Server Notifications v2, Google Play real-time notifications, grace periods, billing retry, refunds, family sharing, free trials, offers, webhooks, migration, self-hosting.
- [Help center](https://revenuedot.app/docs/help) and [blog](https://revenuedot.app/blog): one article per question developers search, with sourced numbers.
- [MCP server](https://github.com/revenuedot/mcp) and [agent skills](https://github.com/revenuedot/agent-skills): the tools an agent uses to set up and run a RevenueDot project.
- **Status in one sentence:** first release v2026.10.03; a real App Store sandbox purchase ran end to end on 2026-10-02; a production app has run RevenueDot beside RevenueCat since 2026-10-02; Cloud has billed real cards since 2026-10-03; self-host is free (AGPL-3.0 server, MIT SDKs) and Cloud is free up to $10,000 a month in tracked revenue, then 0.5% above that, never more than $999 a month.

## Community

- [Discussions](https://github.com/revenuedot/revenuedot/discussions) for questions and ideas, [issues](https://github.com/revenuedot/revenuedot/issues) for bugs.
- [Contributing](https://github.com/revenuedot/.github/blob/main/CONTRIBUTING.md), [security policy](https://github.com/revenuedot/.github/blob/main/SECURITY.md) (security@revenuedot.app) and the [code of conduct](https://github.com/revenuedot/.github/blob/main/CODE_OF_CONDUCT.md).
- Talk to us: [sales@revenuedot.app](mailto:sales@revenuedot.app), or +1 (628) 296-1014 (an AI assistant answers any time and passes messages on).

<sub>RevenueDot is not affiliated with, endorsed by or sponsored by RevenueCat, Inc. "RevenueCat" is a trademark of RevenueCat, Inc., used only to describe compatibility. Vendor facts checked October 2026; sources on every [comparison page](https://revenuedot.app/compare).</sub>
