# Cabinet-X MCP integrations

Official integration packages for your own Cabinet-X kitchen projects. This repository contains only the integration bridge, manifests, instructions and brand assets. It does not contain the Cabinet-X application or solver.

## Distribution status

These are submission packages, not a claim of marketplace approval.

- Claude plugin: path `claude` on `main`.
- OpenAI desktop plugin: path `openai`; submission requires verified publisher identity and approved local MCP eligibility.
- Cursor plugin: repository root, with `.cursor-plugin/plugin.json`.
- Gemini CLI extension: repository root, with `gemini-extension.json`. Install with `gemini extensions install https://github.com/JoshLabs-App/cabinetx-mcp`. Gallery indexing is separate from installation.

## Requirements and boundaries

Node.js 24 or newer, a Cabinet-X account and the Cabinet-X project open on the same computer are required. Pair only your own current project. AI client subscriptions and usage limits apply. This local integration does not run while your computer is off.

The separate remote sales endpoint `https://cabinetx.app/api/sales-mcp` uses OAuth and supports cloud sales consultation; it does not provide cloud design editing. Do not substitute it for this local design bridge.

# Cabinet-X

Work on your own current Cabinet-X kitchen cabinet project from an AI conversation.
Read actual room measurements and cabinet options, change the design through the
normal editor, check the result, and verify cloud saving. Quote and contract tools
work on drafts; sending, signatures and payment remain in Cabinet-X's human controls.

## Requirements and connection

This is a **local desktop integration**, not a cloud connector. You need Node.js 24,
a Cabinet-X account, and a client that can run local STDIO MCP servers. Your AI
client's subscription and usage limits apply. No model API key is sent to Cabinet-X.

1. Install this plugin in a supported desktop client and enable its MCP server.
2. Sign in at https://cabinetx.app/app/ and open your own current project on the same computer.
3. In your AI conversation, ask to connect Cabinet-X. The client calls `cabinetx_connect`.
4. In Cabinet-X, open **AI → Connection settings → External AI / MCP** and choose **Connect external AI**.
5. Ask the AI to confirm connection and summarize the project before making changes.
6. To edit, first obtain editing control in the normal Cabinet-X interface. Read-only,
   stale revision and cloud-conflict protections still apply.

Example prompts:

- Connect Cabinet-X and summarize my current kitchen project without changing anything.
- Read the available finishes for the base cabinets and help me choose one.
- Check my current design and explain the warnings without changing dimensions.
- Read the current quote options and add a $100 included delivery charge to the draft.

Keep the page open. Changing project or account ends the connection; reconnect for the
new project. Only one external client can control the local bridge at a time. After an
uncertain write, read status and current data before retrying. Do not blindly repeat edits.

## Data and permissions

The plugin runs the bundled readable Node.js bridge on your computer, using only
Node's standard library. It listens on `127.0.0.1:43127` only after you ask to connect.
It checks the exact Cabinet-X website origin and a short-lived signed project proof,
verified at `https://cabinetx.app/api/mcp-access`. Login credentials stay in the website.
The bridge relays tool requests to your open page and returns their results to your AI
client. Normal Cabinet-X APIs handle edits and cloud saving. There is no arbitrary
shell, file, source-code, SQL or URL tool, and no access to another user's projects.

Returned project data may contain customer details, measurements, designs and quote
drafts. Your chosen AI client and model provider receive those tool results under
their own privacy and retention policies. Connect only data you are authorised to
share. The bridge does not create a separate durable tool-result log. Your client
may keep conversation history, and Cabinet-X keeps normal project history. Disconnecting
does not erase data already retained by the AI provider. Close the page, disconnect
in Connection settings, or stop the MCP process to end access.

AI checks are not construction or manufacturing certification. Review the actual
design and obtain required professional checks before manufacture or installation.

## Availability

The generated package is for testing and marketplace submission preparation. A ZIP
does not mean that Cabinet-X is listed, approved, or usable in ordinary cloud chat.
OpenAI public local-MCP submissions require an approved partner organisation. Claude
local-MCP distribution uses a plugin, not a remote connector submission.

[Documentation](https://cabinetx.app/mcp/) · [Privacy](https://cabinetx.app/privacy/)
· [Terms](https://cabinetx.app/terms/) · [Support](https://cabinetx.app/support/)

Support: hello@cabinetx.app

## Current-view render

Choose the `current-view-render` MCP prompt or ask “Generate a magazine-quality
render of my current view, keep the layout and sizes unchanged, and save it as the
hero image.” The client receives the actual visible 3D image and a fixed prompt.
Your client's own image generation/editing capability must generate the result;
Cabinet-X does not call a model API. Generation can change details, so inspect the
result before using it. Actual design data, dimensions and manufacturing drawings
are not changed by this workflow.

Clients with local image tools can use the dedicated source/output paths returned
by `cabinetx_render prepare`, then call `save` with a fresh project revision and
request ID. The bridge reads only its own designated output image, never an arbitrary
caller-supplied file path. These temporary image files are removed after confirmed
saving or normal shutdown; expired captures are removed on the next render call.
Raster data URL return is also supported (PNG/JPEG/WebP, maximum 5MB).

If automatic return is unavailable, save the generated image and use Cabinet-X →
Showcase → Images → Import render, then Set as hero. Imports save to the current
browser gallery and the cloud album. Hero selection belongs to this browser and
is used in the next normal quote/showcase publication; published links do not
change until updated normally. Update/restart the MCP bridge/plugin to discover
the new tool and prompt. This does not establish support in every ChatGPT client.

