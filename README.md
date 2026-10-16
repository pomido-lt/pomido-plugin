# Pomido

Pomido helps Claude and ChatGPT research Lithuanian law and financial questions governed by Lithuanian law. Ask about annual leave, consumer rights, taxes, or other Lithuanian rules, in Lithuanian or English. Your AI finds the relevant official documents, explains the rules, and links to the sources so you can check them. You can research the rules in force today or the wording that applied on a past date.

Pomido provides research information, not legal or financial advice.

## What the plugin contains

- **The `pomido-lithuanian-law` skill.** It tells the AI when to use Pomido and when not to, such as for questions about another country's law.
- **The Pomido MCP server at `https://pomido.lt/mcp`.** It exposes three read-only tools:
  - `search-documents` finds passages that match a query, optionally as of a past date.
  - `get-document` returns a document's details and lists its versions over time.
  - `read-document-content` reads passages in order from one version of a document.

## What the plugin sends and where

The plugin connects only to `https://pomido.lt/mcp`. When you use it, your AI sends search queries and document IDs to that server. The plugin runs no local code and stores no data on your machine.

## Account

The MCP server requires a free Pomido account. The first time the plugin connects, it opens the Pomido sign-in page. Sign in or create an account, then select **Install Pomido** to grant access. In Claude Code, run `/mcp` to sign in.

## Example prompts

- "How many days of annual leave am I entitled to in Lithuania if I work five days a week? Cite the source."
- "I sold an apartment in Lithuania that was my declared place of residence for two years. Do I have to pay personal income tax on the sale?"
- "What were Lithuania's annual leave rules under Article 126 of the Labour Code on 1 July 2024? Link to that version."

## Platforms

This repository holds one plugin with a manifest for each platform:

- `.claude-plugin/plugin.json` is the Claude manifest.
- `plugin.json` and `mcp.json` are the ChatGPT manifests, in the [Agent Plugins](https://agent-plugins.org/) format.

Both manifests use the same skill and the same MCP server.

## Links

- Website: https://pomido.lt/
- Privacy policy: https://pomido.lt/privatumo-politika
- Terms of service: https://pomido.lt/naudojimo-salygos

## License

[MIT](LICENSE)
