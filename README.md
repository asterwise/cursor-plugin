# Asterwise

Asterwise is an MCP server for structured Vedic and Western astrology calculations. It exposes 104 read-only tools covering natal and divisional charts, five-level Vimshottari dasha, Ashtakavarga, Shadbala, classical yogas, panchanga and muhurta, KP and Lal Kitab, Ashtakoota and Tamil porutham matchmaking (including Rajju and Vedha vetoes), tropical Western charts, numerology, and tarot, powered by Swiss Ephemeris.

Watch it work: [46-second demo in Claude Desktop](https://youtu.be/Oe17c6pXl8c). Positions are verified against an independent Swiss Ephemeris run at [asterwise.com/proof](https://asterwise.com/proof/).

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

## Try it

Once connected, ask the agent things like:

- "Cast a natal chart for 12 Nov 1985, 06:45, Mumbai, and summarise the Vimshottari dasha running now."
- "Compare these two birth details with Ashtakoota and tell me if Rajju or Vedha applies."
- "What is today's panchanga for Delhi, and when is Rahu Kaal?"
- "Give me a three-card tarot spread on a career question."

## What leaves your machine

Birth details and questions you provide are sent to `mcp.asterwise.com`, which forwards them to `api.asterwise.com` to compute the result. Usage is metered against your Asterwise account. See the [privacy policy](https://asterwise.com/privacy/) and [terms](https://asterwise.com/terms/).

## Usage notes

- Tools are read-only calculation endpoints (`asterwise:read`).
- Free Sandbox tier: 500 API calls per month.
- Product: [https://asterwise.com](https://asterwise.com)
- Docs: [https://docs.asterwise.com](https://docs.asterwise.com)

## For developers

If you are building apps against the same engines outside Cursor, use the Asterwise REST API documented at [https://docs.asterwise.com](https://docs.asterwise.com). This plugin only wires the hosted MCP endpoint into Cursor.
