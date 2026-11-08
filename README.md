# Cabinet-X AI integrations

Local desktop MCP plugins for the user’s own current Cabinet-X project.
Requires Node.js 24 and the Cabinet-X website open on the same computer.

- `claude/`: Claude plugin (submit this folder, not the private product repository).
- `openai/`: OpenAI portable desktop plugin; public local-MCP submission requires approved partner allowlisting.

These are prepared packages, not marketplace approval. Cloud-only chat needs a separate remote MCP/OAuth service, which this repository does not provide.

[Connection guide](https://cabinetx.app/mcp/) · [Privacy](https://cabinetx.app/privacy/) · [Terms](https://cabinetx.app/terms/) · [Support](https://cabinetx.app/support/)

Copyright 2026 Cabinet-X. All rights reserved. See the LICENSE in each plugin folder. No Cabinet-X core or solver source is included.

## Claude Code installation for authorised repository readers

The repository is private during review preparation. With an account that can read it:

```sh
claude plugin marketplace add JoshLabs-App/cabinetx-mcp
claude plugin install cabinetx@cabinetx
```

This registers our private test marketplace; it is not publication in Anthropic’s directory. Node.js 24 is required.
