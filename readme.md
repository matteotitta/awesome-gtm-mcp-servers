![awesome-gtm-mcp-servers cover](.github/cover.png)

# Awesome GTM MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Model Context Protocol servers that connect an AI agent to the go-to-market stack: CRM, enrichment, SEO, ads, analytics, and lifecycle.

Two things are true about this space and neither is obvious from the existing lists.

**The official-server gap has mostly closed.** The July edition of this list said no first-party MCP server existed for Google Ads, Meta Ads, LinkedIn Ads, Semrush, Mixpanel, Google Search Console, Clay, Hunter, Crustdata, Pipedrive, Close, or Klaviyo. That was already wrong for Google Ads and Pipedrive, and it is wrong for eight more now. Ten of the twelve run an official server today. **LinkedIn Ads** and **Google Search Console** are the two still community-only, so those are the ones to vet hardest before you hand a server an API key and a budget.

**Vendors are migrating to hosted.** Ahrefs, PostHog, and Hunter archived their local repos in favour of remote endpoints, and Salesforce retired its local server for hosted servers and skills. HubSpot, Apollo, and Attio are hosted-first with no meaningful public repo, and nearly every official server added since July is hosted only. A repo-only view of this space is already out of date, so hosted servers are listed here as first-class entries.

Every entry was verified against the live GitHub API or the vendor's own docs on 2026-11-08. Entries are alphabetical within each section. Servers marked **Official** are vendor-maintained; everything else is community-built.

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

- [attio-mcp-server](https://github.com/kesslerio/attio-mcp-server) - The most active community Attio server, covering records, lists, and CRM objects. Attio also runs a hosted server at `https://mcp.attio.com/mcp` ([docs](https://docs.attio.com/mcp/overview)). 68 stars.
- [Close MCP Server](https://developer.close.com/mcp) - **Official**, hosted at `mcp.close.com/mcp`. Separate scopes for reading, safe writes, and destructive writes, which is the right shape for a CRM an agent can change. OAuth or API key.
- [close-crm-cli](https://github.com/bcharleson/close-crm-cli) - CLI and MCP server for Close, advertising 160+ commands. Predates Close's official server above and has very low adoption. 1 star.
- [forcedotcom/mcp-hosted](https://github.com/forcedotcom/mcp-hosted) - **Official.** Salesforce's hosted MCP servers, and the first-party MCP path now that the local CLI server below has reached end of life. Apache-2.0. 136 stars.
- [HubSpot MCP Server](https://developers.hubspot.com/mcp) - **Official**, hosted at `mcp.hubspot.com`. Read and write access to CRM objects (contacts, companies, deals, tickets, quotes) and engagements (calls, emails, meetings, notes), plus read-only marketing data. A separate local Developer MCP Server covers the CLI platform. Note: `HubSpot/mcp-server` exists on GitHub under the real org but is an empty placeholder — do not use it.
- [MCP-Salesforce](https://github.com/smn2gnt/MCP-Salesforce) - The most-starred community Salesforce connector after the official one, actively maintained. MIT. 179 stars.
- [mcp-server-salesforce](https://github.com/tsmztech/mcp-server-salesforce) - Community server for querying and manipulating Salesforce records. MIT. 164 stars.
- [Pipedrive MCP Server](https://www.pipedrive.com/en/features/mcp-server) - **Official**, hosted. Read and write access to Pipedrive CRM data over OAuth, on every plan. Launched 30 June 2026. `pipedrive/mcp-server` on GitHub is still a 404; this hosted server is the first-party path.
- [pipedrive-mcp-server (ckalima)](https://github.com/ckalima/pipedrive-mcp-server) - Pipedrive server with 155 contract-tested tools, a v2-first API surface, and gated destructive operations. The strongest community option: more recent than the alternative below and MIT-licensed. 10 stars.
- [pipedrive-mcp-server (WillDent)](https://github.com/WillDent/pipedrive-mcp-server) - The most-starred community Pipedrive server. Last pushed July 2026. 60 stars.
- [salesforcecli/mcp](https://github.com/salesforcecli/mcp) - **Official but archived.** Salesforce's local server reached end of life on 2 November 2026; the npm package still installs but gets no more releases. Salesforce now ships its developer tooling as skills in [forcedotcom/sf-skills](https://github.com/forcedotcom/sf-skills). Historical pointer; use the hosted servers above. Apache-2.0. 488 stars.
- [twenty-crm-mcp-server](https://github.com/mhenry3164/twenty-crm-mcp-server) - Server for Twenty, the open-source CRM. An open CRM plus an open server is the only fully inspectable CRM-agent stack here. 108 stars.

## Enrichment and Data

- [apify/actor-mcp-servers](https://github.com/apify/actor-mcp-servers) - **Official.** Apify's collection of individual scraper-backed servers published as Actors — a directory rather than a single server. MIT. 21 stars.
- [apify/apify-mcp-server](https://github.com/apify/apify-mcp-server) - **Official**, at `mcp.apify.com`. The highest-starred server in this list. Exposes thousands of ready-made scrapers to an agent for extracting data from social media, search engines, maps, and e-commerce. Supports OAuth for URL-only connection plus stdio for local use. Formerly cited as `actors-mcp-server`. MIT. 15,218 stars.
- [Apollo.io MCP Server](https://www.apollo.io/product/mcp) - **Official**, hosted at `mcp.apollo.io`. Lead generation, contact and company enrichment, and sales engagement including search, sequences, and opportunities. OAuth 2.0, so the endpoint itself returns 401 in a browser. Not to be confused with Apollo GraphQL, which publishes an unrelated MCP server under a confusingly similar name.
- [apollo-io-mcp](https://github.com/thevgergroup/apollo-io-mcp) - The most current community Apollo.io server. MIT. 19 stars.
- [Clay MCP](https://www.clay.com/mcp) - **Official**, hosted. Clay's own server, bringing its 150+ data providers, research agents, and your team's Clay functions into Claude, ChatGPT, and Codex. Clay hasn't published a raw endpoint (`mcp.clay.com` does not resolve), so connect through the client's connector directory.
- [Crustdata MCP](https://crustdata.com/mcp-server) - **Official**, hosted. 40 tools for company and people data. The product page and the docs give different connect URLs, so check the [docs](https://docs.crustdata.com/for-agents/mcp) for the current one.
- [Hunter MCP](https://hunter.io/mcp) - **Official**, hosted at `mcp.hunter.io/mcp`. Email finding and verification, with OAuth or an API key. Hunter archived its earlier local repo, `hunter-io/hunter-mcp`, in favour of this remote server.

## SEO and Content

- [ahrefs-mcp-server](https://github.com/ahrefs/ahrefs-mcp-server) - **Official but archived.** Ahrefs' local server, explicitly deprecated in favour of a remote one. Its readme says plainly: no longer maintained, works only with v3 API keys, outdated. Listed as a historical pointer; see the remote server below. 100 stars.
- [Ahrefs Remote MCP Server](https://docs.ahrefs.com/mcp/docs/introduction) - **Official**, hosted at `https://api.ahrefs.com/mcp/mcp`. The current path, replacing the archived local server, with no local setup required. Lite plan and up.
- [dataforseo/mcp-server-typescript](https://github.com/dataforseo/mcp-server-typescript) - **Official.** Exposes the DataForSEO API family — SERP, keywords, backlinks, on-page — to MCP clients. Apache-2.0. 261 stars.
- [dataforseo-mcp-server](https://github.com/Skobyn/dataforseo-mcp-server) - Comprehensive stdio server for the DataForSEO API, as a community alternative to the official one. MIT. 83 stars.
- [exa-labs/exa-mcp-server](https://github.com/exa-labs/exa-mcp-server) - **Official.** Neural web search and crawling, exposing Exa's search and content-retrieval APIs. MIT. 5,216 stars.
- [firecrawl/firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) - **Official.** Scraping, crawling, search, and structured extraction. Note the org rename — `mendableai/firecrawl-mcp-server` redirects here and most lists still cite the stale path. MIT. 7,776 stars.
- [Semrush MCP](https://developer.semrush.com/api/v4/introduction/semrush-mcp/) - **Official**, hosted. Keyword, backlink, traffic, and competitor data from Semrush, also listed as an official app in Claude and ChatGPT.
- [semrush-mcp](https://github.com/mrkooblu/semrush-mcp) - Access to Semrush API data. The most-starred community option, now that Semrush runs its own server above. MIT. 40 stars.
- [spider-rs/spider](https://github.com/spider-rs/spider) - The Spider Rust crawler itself, not an MCP server. Listed as the parent project behind the Spider Cloud server below. MIT. 2,839 stars.
- [spider-cloud-mcp-server](https://github.com/spider-rs/spider-cloud-mcp-server) - **Official.** Server for the Spider Cloud crawling API. Very low stars but first-party. `spider-rs/spider-mcp` redirects here. MIT. 2 stars.

## Analytics and Product

- [amplitude/mcp-server-guide](https://github.com/amplitude/mcp-server-guide) - **Official**, but a guide rather than a server — documentation on using Amplitude's hosted MCP offering. Listed so you do not go looking for source that is not there. 48 stars.
- [googleanalytics/google-analytics-mcp](https://github.com/googleanalytics/google-analytics-mcp) - **Official.** Google's GA4 server and the first-party path for Analytics data. Apache-2.0. 3,683 stars.
- [mcp-gsc](https://github.com/AminForou/mcp-gsc) - The most-starred Search Console server and the de-facto standard, since Google publishes none. MIT. 2,142 stars.
- [mcp-server-gsc](https://github.com/ahonn/mcp-server-gsc) - A lighter, widely-used Search Console alternative. No licence declared. 283 stars.
- [Mixpanel MCP Server](https://docs.mixpanel.com/docs/mcp) - **Official**, hosted at `mcp.mixpanel.com/mcp`. Runs insights, funnel, flow, and retention queries and builds dashboards. No public repo.
- [PostHog/mcp](https://github.com/PostHog/mcp) - **Official but archived.** The former standalone server, now moved into the monorepo. Historical pointer only. MIT. 151 stars.
- [PostHog monorepo services/mcp](https://github.com/PostHog/posthog/tree/master/services/mcp) - **Official**, current. PostHog's server now lives in the monorepo, with a hosted endpoint at `mcp.posthog.com`.
- [surendranb/google-analytics-mcp](https://github.com/surendranb/google-analytics-mcp) - GA4 data with schema discovery, server-side aggregation, and defaults that reduce data wrangling. Actively maintained. Apache-2.0. 244 stars.

## Ads

Google and Meta now run official servers. LinkedIn Ads is still community-only. These tools spend real money, so read the write paths before connecting one.

- [ads-mcp](https://github.com/amekala/ads-mcp) - Cross-platform server covering Google, Meta, LinkedIn, and TikTok Ads with 100+ tools for campaign creation, performance analysis, keyword research, and budget optimisation. Actively maintained; no licence declared. 105 stars.
- [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server) - Server for analysing Google Ads performance data. MIT. 147 stars.
- [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp) - **Official.** Google's own Google Ads server: reporting through GAQL, plus a few asset and label writes that need a confirm step. Google's docs page still calls it read-only, so check the repo for the current tools. Apache-2.0. 1,128 stars.
- [linkedin-ads-mcp](https://github.com/danielpopamd/linkedin-ads-mcp) - One of the only dedicated LinkedIn Ads servers. MIT. 42 stars.
- [markifact-mcp](https://github.com/markifact/markifact-mcp) - Spans Google, Meta, GA4, TikTok, and LinkedIn Ads with 300+ operations, and notably requires human-in-the-loop on every write. Given that much of this category can spend budget unsupervised, that design choice is the reason to look here first. MIT. 57 stars.
- [Meta Ads MCP Server](https://www.facebook.com/business/tools/ads-mcp-server) - **Official**, hosted at `mcp.facebook.com/ads`. Creates, manages, and reports on Facebook and Instagram campaigns.
- [meta-ads-mcp (mikusnuz)](https://github.com/mikusnuz/meta-ads-mcp) - Server for Meta Marketing API v25.0 with 135 tools for Facebook and Instagram campaigns. MIT. 94 stars.
- [meta-ads-mcp (pipeboard-co)](https://github.com/pipeboard-co/meta-ads-mcp) - The most-starred community Meta Ads option, part of a five-platform family with a hosted remote server and a free plan. Non-standard licence. 1,358 stars.

## Email and Lifecycle

- [Instantly MCP](https://help.instantly.ai/en/articles/12980002-instantly-mcp-model-context-protocol) - **Official**, hosted at `mcp.instantly.ai/mcp`. 31 tools, included with a subscription.
- [instantly-cli](https://github.com/bcharleson/instantly-cli) - CLI and MCP server for the Instantly cold-email platform. The most-starred community option. 38 stars.
- [kit-mcp](https://github.com/dancumberland/kit-mcp) - Kit (formerly ConvertKit) server claiming full v4 API coverage across 13 tools, with engagement analytics and broadcast click tracking. Kit also runs a hosted server. MIT. 2 stars.
- [Klaviyo MCP Server](https://developers.klaviyo.com/en/docs/klaviyo_mcp_server) - **Official.** A remote server at `mcp.klaviyo.com/mcp` (OAuth) plus a local one. Has a read-only flag, which is worth turning on before you let an agent near a live list.
- [resend/resend-mcp](https://github.com/resend/resend-mcp) - **Official.** Sending email and interacting with the Resend API. Note the rename: `resend/mcp-send-email` redirects here. MIT. 580 stars.
- [Smartlead MCP Server](https://helpcenter.smartlead.ai/en/articles/300-smartlead-mcp-server) - **Official**, hosted. SSE only, with the API key in the URL, so treat the URL like a password. Replaces the community servers this list carried in July, both now archived or abandoned.

## Comms and Ops

- [Calendly MCP Server](https://developer.calendly.com/docs/mcp/calendly-mcp-server) - **Official**, fully hosted by Calendly at `mcp.calendly.com`. Self-hosting is not supported.
- [google_workspace_mcp](https://github.com/taylorwilsdon/google_workspace_mcp) - The de-facto community standard for Workspace, covering Gmail, Calendar, Docs, Sheets, Slides, Chat, Forms, Tasks, and Drive, shipping as both a server and a CLI. MIT. 3,483 stars.
- [Linear MCP Server](https://linear.app/docs/mcp) - **Official**, hosted at `mcp.linear.app/mcp`, with a separate read-only endpoint at `/mcp/readonly`.
- [linear-mcp](https://github.com/tacticlaunch/mcp-linear) - Community server to retrieve, create, and update Linear issues, projects, and teams in natural language. MIT. 149 stars.
- [makenotion/notion-mcp-server](https://github.com/makenotion/notion-mcp-server) - **Official.** Notion pages, databases, and search. One of the highest-adoption official servers in the ecosystem. MIT. 4,699 stars.
- [mcp-notion-server](https://github.com/suekou/mcp-notion-server) - A widely-used community Notion server that predates and parallels the official one. MIT. 924 stars.
- [slackapi/slack-skills-plugin](https://github.com/slackapi/slack-skills-plugin) - **Official.** Slack's own plugin for Claude Code and Cursor, bundling a Slack MCP server plus developer skills. The first-party Slack path. MIT. 165 stars.
- [slack-mcp-server (korotovsky)](https://github.com/korotovsky/slack-mcp-server) - The most-starred Slack server, with Apps support, GovSlack, DMs, and smart history fetching, needing no permission requests. MIT. 1,889 stars.
- [slack-mcp-server (ubie-oss)](https://github.com/ubie-oss/slack-mcp-server) - The most permissively-licensed maintained Slack option. Apache-2.0. 110 stars.

## Registries

- [awesome-agentic-advertising](https://github.com/jshorwitz/awesome-agentic-advertising) - Curated servers, tools, and protocols for AI-powered advertising across Google, Meta, LinkedIn, Reddit, TikTok, and Amazon. The closest neighbour to this list and narrower than GTM. 46 stars.
- [awesome-claude-code-for-gtm](https://github.com/matteotitta/awesome-claude-code-for-gtm) - The companion list: Claude Code skills, agents, and workflows for go-to-market work, of which the servers here are one layer.
- [modelcontextprotocol/registry](https://github.com/modelcontextprotocol/registry) - **Official.** The community-driven registry service, and the successor to the old in-readme integrations list. 7,453 stars.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) - **Official.** The canonical reference servers maintained by the MCP steering group. It no longer carries a third-party integrations list, which is the gap this list exists to fill. 91,859 stars.
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) - The largest MCP list by stars, broader than this one and covering the whole ecosystem. MIT. 97,450 stars.
- [wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers) - A curated, actively-maintained list pairing with the mcp.so directory. MIT. 4,405 stars.

## Known Gaps

Stated rather than padded, because knowing a thing does not exist is worth as much as a link.

**LinkedIn Ads** has no first-party server; the community servers in the Ads section are the whole category. **Google Search Console** is the same: Google's own [MCP index](https://github.com/google/mcp) lists Analytics but not Search Console, and there is an [open request](https://github.com/google/mcp/issues/17) for one. Both are "not found" rather than proven absent, so check again before you build your own. **Clay** runs an official server but publishes no raw endpoint, which matters if your client can only connect by URL.

The pattern has reversed since July. Most of the vendors closest to revenue have now shipped a server, and almost all of them chose hosted. The work has moved from finding a server to deciding which write scopes to grant it.
