# Magic MCP (21st.dev)

This project is configured with the [Magic MCP server](https://github.com/21st-dev/magic-mcp) via the root `.mcp.json`. Magic generates modern UI components (buttons, forms, dashboards, etc.) from natural-language descriptions, backed by the 21st.dev component library.

## Setup

1. Get an API key from the [21st.dev Magic Console](https://21st.dev/magic/console).
2. Export it before starting Claude Code:

   ```bash
   export TWENTY_FIRST_API_KEY="your-api-key"
   ```

   The `.mcp.json` config expands `${TWENTY_FIRST_API_KEY}` into the `API_KEY` environment variable the server expects, so the key never lives in the repo.

3. Start Claude Code in this repo and approve the project MCP server when prompted. Requires Node.js (the server runs via `npx -y @21st-dev/magic@latest`).

## Usage

Ask for a UI component and mention Magic, or use the `/ui` trigger in your prompt, e.g.:

```
/ui create a modern navigation bar with responsive design
```

The server exposes tools for component generation, component inspiration search, and logo integration (SVGL).
