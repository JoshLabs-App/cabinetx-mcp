# OpenCabinet — Cloud Kitchen Layout, 2D Plan & Retail Quote MCP

**OpenCabinet** (`https://opencabinetai.com/api/sales-mcp`) is the official remote Streamable HTTP **Model Context Protocol (MCP)** connector powered by **[Cabinet-X](https://cabinetx.app)**.

Connect ChatGPT, Claude, Cursor, VS Code / GitHub Copilot, Google Gemini CLI, and Mistral with **zero local helper software** via standard **OAuth 2.1 + PKCE + Dynamic Client Registration**.

## Remote MCP Endpoint

```text
https://opencabinetai.com/api/sales-mcp
```

## 1-Click / Instant Platform Setup

- **Web Hub & 1-Click Links**: [https://opencabinetai.com/](https://opencabinetai.com/)
- **ChatGPT (Web, Desktop & Mobile)**: Open `Settings → Connectors → Create`, paste `https://opencabinetai.com/api/sales-mcp`, and approve OAuth.
- **Claude (Web, Desktop & Mobile)**: [1-Click Add OpenCabinet in Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=OpenCabinet&connectorUrl=https%3A%2F%2Fopencabinetai.com%2Fapi%2Fsales-mcp)
- **Claude Code**:
  ```bash
  claude mcp add --transport http opencabinet https://opencabinetai.com/api/sales-mcp
  ```
- **Cursor**: Open `https://opencabinetai.com/` and click **1-Click Install in Cursor**, or install from the Cursor Marketplace.
- **VS Code & GitHub Copilot**: Search `@mcp opencabinet` in Extensions (`com.opencabinetai/opencabinet` on the Official MCP Registry) or click **1-Click VS Code / Copilot** on `https://opencabinetai.com/`.
- **Google Gemini CLI**:
  ```bash
  gemini extensions install https://github.com/JoshLabs-App/opencabinet
  # or directly:
  gemini mcp add --transport http opencabinet https://opencabinetai.com/api/sales-mcp
  ```

## Capabilities

1. **`cabinetx_cloud_generate`** — Create a cloud kitchen project from room wall measurements, openings, appliances, or sketch summaries and run the deterministic Cabinet-X server layout solver; returns an interactive 2D plan widget (`ui://cabinetx/design-card.html`), customer-safe retail quote estimate, and direct 3D Studio link.
2. **`cabinetx_mobile_design`** — Inspect designs, query real catalog finishes/door styles, and apply revision-checked edits (`set_color`, `set_door_style`, `resize_cabinet`, `add_island`, `delete_item`).
3. **`cabinetx_sales_search` / `cabinetx_sales_project_context` / `cabinetx_sales_followup_draft` / `cabinetx_sales_save_followup` / `cabinetx_sales_capabilities`** — Owner-scoped customer project lookup and follow-up workflow.

## Links

- Homepage: [https://opencabinetai.com](https://opencabinetai.com)
- 3D Studio: [https://cabinetx.app/app/](https://cabinetx.app/app/)
- Privacy Policy: [https://opencabinetai.com/privacy/](https://opencabinetai.com/privacy/)
- Terms of Service: [https://opencabinetai.com/terms/](https://opencabinetai.com/terms/)
- Support: [https://opencabinetai.com/support/](https://opencabinetai.com/support/)
