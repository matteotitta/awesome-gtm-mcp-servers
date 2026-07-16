# Awesome GTM MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Model Context Protocol servers that connect an AI agent to the go-to-market stack: CRM, enrichment, SEO, ads, analytics, and lifecycle.

Two things are true about this space and neither is obvious from the existing lists.

**The official-server gap is the story.** No first-party MCP server exists for Google Ads, Meta Ads, LinkedIn Ads, Semrush, Mixpanel, Google Search Console, Clay, Hunter, Crustdata, Pipedrive, or Close. Go-to-market's highest-spend surfaces are entirely community-built. That is worth knowing before you hand one of them an API key and a budget.

**Vendors are migrating to hosted.** Ahrefs and PostHog both archived their local repos in favour of remote endpoints. HubSpot, Apollo, and Attio are hosted-first with no meaningful public repo. A repo-only view of this space is already out of date, so hosted servers are listed here as first-class entries.

Every entry was verified against the live GitHub API or the vendor's own docs on 2026-07-16. Entries are alphabetical within each section. Servers marked **Official** are vendor-maintained; everything else is community-built.

## Contents

- [CRM](#crm)
- [Enrichment and Data](#enrichment-and-data)
- [SEO and Content](#seo-and-content)
- [Analytics and Product](#analytics-and-product)
- [Ads](#ads)
- [Email and Lifecycle](#email-and-lifecycle)
- [Comms and Ops](#comms-and-ops)
- [Registries](#registries)
- [Known Gaps](#known-gaps)

---

## CRM

- [attio-mcp-server](https://github.com/kesslerio/attio-mcp-server) - The most active community Attio server, covering records, lists, and CRM objects. Attio also runs a hosted server at `mcp.attio.com`; check their docs for the canonical connect URL. 69 stars.
- [close-crm-cli](https://github.com/bcharleson/close-crm-cli) - CLI and MCP server for Close, advertising 160+ commands. The only maintained Close option found, with very low adoption. 1 star.
- [forcedotcom/mcp-hosted](https://github.com/forcedotcom/mcp-hosted) - Salesforce's hosted MCP servers, the remote counterpart to the CLI server below for teams who prefer a managed endpoint. Apache-2.0. 125 stars.
- [HubSpot MCP Server](https://developers.hubspot.com/mcp) - **Official**, hosted at `mcp.hubspot.com`. Read and write access to CRM objects (contacts, companies, deals, tickets, quotes) and engagements (calls, emails, meetings, notes), plus read-only marketing data. A separate local Developer MCP Server covers the CLI platform. Note: `HubSpot/mcp-server` exists on GitHub under the real org but is an empty placeholder — do not use it.
- [mcp-hubspot](https://github.com/baryhuang/mcp-hubspot) - Community HubSpot server with vector storage and caching to work around API limits. Last pushed November 2025; prefer the official hosted server. MIT. 128 stars.
- [MCP-Salesforce](https://github.com/smn2gnt/MCP-Salesforce) - The most-starred community Salesforce connector after the official one, actively maintained. MIT. 178 stars.
- [mcp-server-salesforce](https://github.com/tsmztech/mcp-server-salesforce) - Community server for querying and manipulating Salesforce records. MIT. 162 stars.
- [pipedrive-mcp-server (ckalima)](https://github.com/ckalima/pipedrive-mcp-server) - Pipedrive server with 155 contract-tested tools, a v2-first API surface, and gated destructive operations. Fewer stars than the alternative below but substantially more recent and MIT-licensed. 8 stars.
- [pipedrive-mcp-server (WillDent)](https://github.com/WillDent/pipedrive-mcp-server) - The most-starred Pipedrive server. No licence declared and no push since October 2025. 57 stars.
- [salesforcecli/mcp](https://github.com/salesforcecli/mcp) - **Official.** Salesforce's server, maintained by the CLI team, running locally against authenticated orgs. The actively-maintained first-party path. Apache-2.0. 440 stars.
- [twenty-crm-mcp-server](https://github.com/mhenry3164/twenty-crm-mcp-server) - Server for Twenty, the open-source CRM. An open CRM plus an open server is the only fully inspectable CRM-agent stack here. 68 stars.

## Enrichment and Data

- [apify/actor-mcp-servers](https://github.com/apify/actor-mcp-servers) - **Official.** Apify's collection of individual scraper-backed servers published as Actors — a directory rather than a single server. MIT. 20 stars.
- [apify/apify-mcp-server](https://github.com/apify/apify-mcp-server) - **Official**, at `mcp.apify.com`. Exposes thousands of ready-made scrapers to an agent for extracting data from social media, search engines, maps, and e-commerce. Supports OAuth for URL-only connection plus stdio for local use. Formerly cited as `actors-mcp-server`. MIT. 1,963 stars.
- [Apollo.io MCP Server](https://www.apollo.io/product/mcp) - **Official**, hosted at `mcp.apollo.io`. Lead generation, contact and company enrichment, and sales engagement including search, sequences, and opportunities. OAuth 2.0, so the endpoint itself returns 401 in a browser. Not to be confused with Apollo GraphQL, which publishes an unrelated MCP server under a confusingly similar name.
- [apollo-io-mcp](https://github.com/thevgergroup/apollo-io-mcp) - The most current community Apollo.io server. MIT. 19 stars.
- [apollo-io-mcp-server](https://github.com/lkm1developer/apollo-io-mcp-server) - TypeScript community server wrapping the Apollo.io API. Stale since April 2025; prefer the official hosted server. MIT. 40 stars.
- [clay-mcp](https://github.com/mesh/clay-mcp) - The only Clay server found. Clay publishes no official MCP server and `mcp.clay.com` does not resolve, so this is the whole category. No licence declared. 33 stars.
- [peopledatalabs-mcp](https://github.com/phxdev1/peopledatalabs-mcp) - Person and company enrichment through People Data Labs. Very low adoption, stale since April 2025, and the only PDL option found. Apache-2.0. 2 stars.

## SEO and Content

- [ahrefs-mcp-server](https://github.com/ahrefs/ahrefs-mcp-server) - **Official but archived.** Ahrefs' local server, explicitly deprecated in favour of a remote one. Its readme says plainly: no longer maintained, works only with v3 API keys, outdated. Listed as a historical pointer; see the remote server below. 100 stars.
- [Ahrefs Remote MCP Server](https://docs.ahrefs.com/docs/mcp) - **Official**, hosted. The current path, replacing the archived local server, with no local setup required.
- [dataforseo/mcp-server-typescript](https://github.com/dataforseo/mcp-server-typescript) - **Official.** Exposes the DataForSEO API family — SERP, keywords, backlinks, on-page — to MCP clients. Apache-2.0. 231 stars.
- [dataforseo-mcp-server](https://github.com/Skobyn/dataforseo-mcp-server) - Comprehensive stdio server for the DataForSEO API, as a community alternative to the official one. MIT. 80 stars.
- [exa-labs/exa-mcp-server](https://github.com/exa-labs/exa-mcp-server) - **Official.** Neural web search and crawling, exposing Exa's search and content-retrieval APIs. MIT. 4,728 stars.
- [firecrawl/firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) - **Official.** Scraping, crawling, search, and structured extraction; the highest-starred server in this list. Note the org rename — `mendableai/firecrawl-mcp-server` redirects here and most lists still cite the stale path. MIT. 6,969 stars.
- [semrush-mcp](https://github.com/mrkooblu/semrush-mcp) - Access to Semrush API data. Semrush publishes no official server; this is the most-starred community option. MIT. 37 stars.
- [spider-rs/spider](https://github.com/spider-rs/spider) - The Spider Rust crawler itself, not an MCP server. Listed as the parent project behind the Spider Cloud server below. MIT. 2,604 stars.
- [spider-cloud-mcp-server](https://github.com/spider-rs/spider-cloud-mcp-server) - **Official.** Server for the Spider Cloud crawling API. Very low stars but first-party. `spider-rs/spider-mcp` redirects here. MIT. 2 stars.

## Analytics and Product

- [amplitude/mcp-server-guide](https://github.com/amplitude/mcp-server-guide) - **Official**, but a guide rather than a server — documentation on using Amplitude's hosted MCP offering. Listed so you do not go looking for source that is not there. 45 stars.
- [googleanalytics/google-analytics-mcp](https://github.com/googleanalytics/google-analytics-mcp) - **Official.** Google's GA4 server and the first-party path for Analytics data. Apache-2.0. 2,687 stars.
- [mcp-gsc](https://github.com/AminForou/mcp-gsc) - The most-starred Search Console server and the de-facto standard, since Google publishes none. MIT. 1,174 stars.
- [mcp-server-gsc](https://github.com/ahonn/mcp-server-gsc) - A lighter, widely-used Search Console alternative. No licence declared. 248 stars.
- [mixpanel-mcp](https://github.com/dragonkhoi/mixpanel-mcp) - The most-starred Mixpanel server. Mixpanel publishes none officially, and this is stale since March 2025. MIT. 19 stars.
- [PostHog/mcp](https://github.com/PostHog/mcp) - **Official but archived.** The former standalone server, now moved into the monorepo. Historical pointer only. MIT. 151 stars.
- [PostHog monorepo services/mcp](https://github.com/PostHog/posthog/tree/master/services/mcp) - **Official**, current. PostHog's server now lives in the monorepo, with a hosted endpoint at `mcp.posthog.com`.
- [surendranb/google-analytics-mcp](https://github.com/surendranb/google-analytics-mcp) - GA4 data with schema discovery, server-side aggregation, and defaults that reduce data wrangling. Actively maintained. Apache-2.0. 228 stars.

## Ads

Everything in this category is community-built. No first-party server exists for Google Ads, Meta Ads, or LinkedIn Ads. These tools spend real money, so read the write paths before connecting one.

- [ads-mcp](https://github.com/amekala/ads-mcp) - Cross-platform server covering Google, Meta, LinkedIn, and TikTok Ads with 100+ tools for campaign creation, performance analysis, keyword research, and budget optimisation. Actively maintained; no licence declared. 70 stars.
- [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server) - Server for analysing Google Ads performance data. MIT. 135 stars.
- [linkedin-ads-mcp](https://github.com/danielpopamd/linkedin-ads-mcp) - One of the only dedicated LinkedIn Ads servers. MIT. 24 stars.
- [markifact-mcp](https://github.com/markifact/markifact-mcp) - Spans Google, Meta, GA4, TikTok, and LinkedIn Ads with 300+ operations, and notably requires human-in-the-loop on every write. Given that the rest of this category can spend budget unsupervised, that design choice is the reason to look here first. MIT. 51 stars.
- [mcp-google-ads](https://github.com/cohnen/mcp-google-ads) - The most-starred dedicated Google Ads server, for natural-language analysis of campaigns, performance, and keywords. No push since October 2025. MIT. 668 stars.
- [meta-ads-mcp (mikusnuz)](https://github.com/mikusnuz/meta-ads-mcp) - Server for Meta Marketing API v25.0 with 135 tools for Facebook and Instagram campaigns. MIT. 58 stars.
- [meta-ads-mcp (pipeboard-co)](https://github.com/pipeboard-co/meta-ads-mcp) - The most-starred Meta Ads option, part of a five-platform family with a hosted remote server and a free plan. Non-standard licence. 1,082 stars.

## Email and Lifecycle

- [instantly-cli](https://github.com/bcharleson/instantly-cli) - CLI and MCP server for the Instantly cold-email platform. The most-starred Instantly option; no official server exists. 29 stars.
- [kit-mcp](https://github.com/dancumberland/kit-mcp) - Kit (formerly ConvertKit) server claiming full v4 API coverage across 13 tools, with engagement analytics and broadcast click tracking. Kit also runs a hosted server. MIT. 2 stars.
- [resend/resend-mcp](https://github.com/resend/resend-mcp) - **Official.** Sending email and interacting with the Resend API. Note the rename: `resend/mcp-send-email` redirects here. MIT. 553 stars.
- [smartlead-mcp-server (jonathan-politzki)](https://github.com/jonathan-politzki/smartlead-mcp-server) - Local-deployment Smartlead server. The most viable Smartlead option given the archive below, but stale since July 2025. 17 stars.
- [smartlead-mcp-server (LeadMagic)](https://github.com/LeadMagic/smartlead-mcp-server) - **Archived.** Formerly the most complete Smartlead server with 113 tools. Do not present as maintained. MIT. 22 stars.

## Comms and Ops

- [calendly-mcp-server](https://github.com/meAmitPatil/calendly-mcp-server) - Open-source Calendly server. Calendly appears to run a hosted server; prefer that where possible. MIT. 10 stars.
- [google_workspace_mcp](https://github.com/taylorwilsdon/google_workspace_mcp) - The de-facto community standard for Workspace, covering Gmail, Calendar, Docs, Sheets, Slides, Chat, Forms, Tasks, and Drive, shipping as both a server and a CLI. MIT. 2,857 stars.
- [linear-mcp](https://github.com/tacticlaunch/mcp-linear) - Retrieve, create, and update Linear issues, projects, and teams in natural language. More recent than the alternative below. MIT. 143 stars.
- [linear-mcp-server](https://github.com/jerhadf/linear-mcp-server) - The most-starred Linear server, stale since May 2025. Linear also runs an official hosted server. MIT. 346 stars.
- [makenotion/notion-mcp-server](https://github.com/makenotion/notion-mcp-server) - **Official.** Notion pages, databases, and search. One of the highest-adoption official servers in the ecosystem. MIT. 4,531 stars.
- [mcp-notion-server](https://github.com/suekou/mcp-notion-server) - A widely-used community Notion server that predates and parallels the official one. MIT. 913 stars.
- [slackapi/slack-skills-plugin](https://github.com/slackapi/slack-skills-plugin) - **Official.** Slack's own plugin for Claude Code and Cursor, bundling a Slack MCP server plus developer skills. The first-party Slack path. MIT. 83 stars.
- [slack-mcp-server (korotovsky)](https://github.com/korotovsky/slack-mcp-server) - The most-starred Slack server, with Apps support, GovSlack, DMs, and smart history fetching, needing no permission requests. MIT. 1,731 stars.
- [slack-mcp-server (ubie-oss)](https://github.com/ubie-oss/slack-mcp-server) - The most permissively-licensed maintained Slack option. Apache-2.0. 110 stars.
- [slack-mcp-server (zencoderai)](https://github.com/zencoderai/slack-mcp-server) - The server the official MCP servers readme points to as successor to the archived reference implementation. Low stars and stale since July 2025 despite that endorsement. 72 stars.

## Registries

- [appcypher/awesome-mcp-servers](https://github.com/appcypher/awesome-mcp-servers) - The second-biggest general list. No licence declared. 5,686 stars.
- [awesome-agentic-advertising](https://github.com/jshorwitz/awesome-agentic-advertising) - Curated servers, tools, and protocols for AI-powered advertising across Google, Meta, LinkedIn, Reddit, TikTok, and Amazon. The closest neighbour to this list and narrower than GTM. 29 stars.
- [awesome-claude-code-for-gtm](https://github.com/matteotitta/awesome-claude-code-for-gtm) - The companion list: Claude Code skills, agents, and workflows for go-to-market work, of which the servers here are one layer.
- [modelcontextprotocol/registry](https://github.com/modelcontextprotocol/registry) - **Official.** The community-driven registry service, and the successor to the old in-readme integrations list. 7,027 stars.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) - **Official.** The canonical reference servers maintained by the MCP steering group. It no longer carries a third-party integrations list, which is the gap this list exists to fill. 88,543 stars.
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) - The largest MCP list by stars, broader than this one and covering the whole ecosystem. MIT. 90,842 stars.
- [wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers) - A curated, actively-maintained list pairing with the mcp.so directory. MIT. 4,208 stars.

## Known Gaps

Stated rather than padded, because knowing a thing does not exist is worth as much as a link.

**Clay** publishes no official server, and `mcp.clay.com` does not resolve. The single community option above is the whole category. **Crustdata** and **Hunter.io** are the same story but worse: every community result found was a demo, abandoned, or under five stars, so none are listed here rather than pad the count. **Klaviyo** has no verifiable public endpoint; `mcp.klaviyo.com` returns 404 and the best community option found had six stars. **Close** and **Pipedrive** publish nothing first-party, and `pipedrive/mcp-server` is a 404 despite being widely assumed to exist.

The pattern is consistent: the vendors whose products cost the most and touch revenue most directly are the ones that have shipped the least. If you need one of these, budget for writing it yourself.
