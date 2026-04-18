# AdWeave MCP Server

The MCP server that powers the [AdWeave Claude Code plugin](https://github.com/adweave-ai/adweave-claude-plugin). Covers Meta Ads campaign management **plus** AdWeave-specific workflow tools — brand context, avatars, beliefs, offer brief, methodology library, and competitor intelligence.

60+ tools in one MCP endpoint. Use it standalone from Claude Desktop / Cursor / any MCP client, or let the [AdWeave plugin](https://github.com/adweave-ai/adweave-claude-plugin) orchestrate it for you via opinionated slash commands.

## Quick setup (standalone)

Add this to your MCP client config:

```json
{
  "mcpServers": {
    "adweave": {
      "url": "https://mcp.adweave.ai/meta-ads-mcp",
      "headers": {
        "Authorization": "Bearer <YOUR_ADWEAVE_API_TOKEN>"
      }
    }
  }
}
```

Get your API token at [adweave.ai](https://adweave.ai) (free tier: 50 calls/month).

> If you'd rather use OAuth and pre-built slash commands for daily creative generation, metrics feedback, ad launch, creative production, and competitor research — install the [AdWeave plugin](https://github.com/adweave-ai/adweave-claude-plugin) instead.

## Tools

### Campaign management
- Create, update, duplicate, and manage campaigns / ad sets / ads
- Bulk operations across multiple ad accounts

### Creative management
- Upload images and videos
- Build single-image and carousel creatives
- List previously uploaded creatives

### Audience targeting
- Search interests, behaviors, demographics, geolocations
- Estimate audience size before launch

### Performance insights
- Pull campaign / ad set / ad-level insights
- Demographic and placement breakdowns
- Bulk insights across many ads in one call

### Brand context (AdWeave-specific)
- `list_brands`, `set_brand_context`, `get_current_brand_context`, `get_brand_profile`
- Brand profile includes ad account IDs, page/IG IDs, pixel, landing URL, colors, fonts, voice notes

### AdWeave AI foundation
- `get_avatars` — buyer personas with rich evidence, scoped to your org
- `get_offer_brief` — product / pricing / funnel / differentiation data
- `get_beliefs` — Phase-1 and Phase-2 beliefs, auto-synthesized via Claude if unset
- `get_research_notes` — aggregated avatar evidence + competitor context

### Methodology library
- `get_adweave_methodology` — AdWeave's argumentation framework, copy rules, two-phase belief system, image-generation guide, Meta safe zones, and per-skill procedures. Served auth-gated.

### Competitor intelligence
- `get_competitor_intelligence` — live competitor ad summaries from the AdWeave discovery pipeline (Meta Ad Library scraping + LLM pattern analysis)

### Instagram
- Post to Instagram, fetch creator media, creator insights

## Transport & auth

| Property | Value |
|---|---|
| Protocol | MCP (Model Context Protocol) |
| Transport | Streamable HTTP |
| Auth | API Token (`aw_` prefix) or OAuth |
| Endpoint | `https://mcp.adweave.ai/meta-ads-mcp` |
| Connector name | `adweave` |

## Pricing

| Plan | Calls / month |
|---|---|
| Free | 50 |
| Starter | 500 |
| Pro | Unlimited |

See [adweave.ai/pricing](https://adweave.ai/pricing) for current pricing.

## Links

- [Plugin](https://github.com/adweave-ai/adweave-claude-plugin) — opinionated Claude Code plugin that wraps this MCP in six slash commands
- [Website](https://adweave.ai)
- [Pricing](https://adweave.ai/pricing)
- [MCP Registry](https://registry.modelcontextprotocol.io) — `ai.adweave/adweave-mcp`

## License

MIT
