# AdWeave — Meta Ads MCP Server

Meta Ads MCP server with 47 tools for campaigns, creatives, audiences, and insights.

Connect Claude, Cursor, or any MCP client directly to the Meta Marketing API. Create and manage campaigns, upload creatives, pull performance insights, target audiences, run bulk operations — plus AI-powered campaign diagnosis and buyer persona generation.

## Quick Setup

Add this to your MCP client config:

```json
{
  "mcpServers": {
    "adweave-meta-ads": {
      "url": "https://mcp.adweave.ai/meta-ads-mcp",
      "headers": {
        "Authorization": "Bearer <YOUR_ADWEAVE_API_TOKEN>"
      }
    }
  }
}
```

Get your API token at [adweave.ai](https://adweave.ai) (free tier: 50 calls/month).

## Tools (47)

### Campaign Management
- Create, update, duplicate, and manage campaigns
- Create, update, and manage ad sets
- Create, update, and manage ads
- Bulk operations across multiple ad accounts

### Creative Management
- Upload images and videos
- Build single-image creatives
- Build carousel creatives

### Audience Targeting
- Search interests and behaviors
- Search geolocations
- Estimate audience size before launch

### Performance Insights
- Pull campaign, ad set, and ad-level insights
- Demographic breakdowns
- Placement breakdowns

### AI Intelligence
- **Campaign Intelligence** — AI-powered diagnosis of your funnel performance
- **Customer Avatars** — Buyer persona generation from your actual ad data

## Transport & Auth

| Property | Value |
|---|---|
| **Protocol** | MCP (Model Context Protocol) |
| **Transport** | Streamable HTTP |
| **Auth** | API Token (`aw_` prefix) or OAuth |
| **Endpoint** | `https://mcp.adweave.ai/meta-ads-mcp` |

## Pricing

| Plan | Calls/month | Price |
|---|---|---|
| Free | 50 | $0 |
| Pro | 5,000 | See [pricing](https://adweave.ai/pricing) |
| Team | 25,000 | See [pricing](https://adweave.ai/pricing) |

## Links

- [Website](https://adweave.ai)
- [Pricing](https://adweave.ai/pricing)
- [MCP Registry](https://registry.modelcontextprotocol.io) — `ai.adweave/meta-ads-mcp`

## License

MIT
