# Asterwise

Asterwise is an MCP server for structured Vedic and Western astrology calculations. It exposes 103 read-only tools covering natal and divisional charts, five-level Vimshottari dasha, Ashtakavarga, Shadbala, classical yogas, panchanga and muhurta, KP and Lal Kitab, Ashtakoota and Tamil porutham matchmaking (including Rajju and Vedha vetoes), tropical Western charts, numerology, and tarot, powered by Swiss Ephemeris.

## Install

### Cursor Marketplace (pending listing)

Once listed, install **Asterwise** from the Cursor Marketplace. After install, complete OAuth sign-in when prompted so the agent can call tools with your Asterwise account.

### Manual fallback

Add this MCP server in Cursor (or place the same block in your MCP config):

```json
{
  "mcpServers": {
    "asterwise": {
      "url": "https://mcp.asterwise.com/mcp"
    }
  }
}
```

Then connect and finish OAuth sign-in in the browser consent flow.

## Usage notes

- Tools are read-only calculation endpoints (`asterwise:read`).
- Free Sandbox tier: 500 API calls per month.
- Product: [https://asterwise.com](https://asterwise.com)
- Docs: [https://docs.asterwise.com](https://docs.asterwise.com)

## For developers

If you are building apps against the same engines outside Cursor, use the Asterwise REST API documented at [https://docs.asterwise.com](https://docs.asterwise.com). This plugin only wires the hosted MCP endpoint into Cursor.
