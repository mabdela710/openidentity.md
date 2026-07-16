# OpenIdentity v0.1 Specification

## 1. Purpose

OpenIdentity is a portable identity manifest for AI agents. It combines identity, human verification, roles, skills, MCP tools, A2A metadata, memory discovery links, wallet references, and authorization pointers into one secure, shareable file.

Short form: **OpenIdentity is the discovery layer for AI agent identity.**

USB metaphor: **Like a USB descriptor for an AI agent, OpenIdentity lets any compatible platform understand what the agent is, who controls it, what it can do, and where its approved memory and tools live.**

## 2. Canonical File Name

The recommended canonical file name is:

```text
openidentity.md
```

## 3. Required Fields

| Field | Type | Description |
|---|---|---|
| `openidentity` | string | Manifest version, starting with `0.1`. |
| `agent.id` | string | Stable identifier for the AI agent. |
| `agent.name` | string | Human-readable agent name. |
| `agent.type` | string | Agent type, usually `ai-agent`. |
| `controller` | object | Human, organization, or system controlling the agent. |
| `capabilities.roles` | array | Approved high-level roles. |
| `capabilities.skills` | array | Approved skills or skill families. |

## 4. Recommended Optional Fields

| Field | Type | Description |
|---|---|---|
| `verification` | object | Domain, human, wallet, or signature verification references. |
| `mcp_tools` | array | Approved MCP server and tool references. |
| `a2a` | object | Agent-to-agent metadata and endpoints. |
| `discovery.memory` | array | Approved memory discovery links. |
| `wallets` | array | Wallet references, not private keys. |
| `authorization` | object | Policy, grant, scope, and delegation pointers. |
| `links` | object | Homepage, repository, support, or AxiomID profile links. |

## 5. Security Requirements

- Private keys, secrets, tokens, and private memory content MUST NOT be embedded in the manifest.
- Memory entries SHOULD be references with access labels and policy pointers.
- Controllers SHOULD publish verification references.
- Platforms SHOULD treat unsigned manifests as discovery hints, not final proof of authority.
- Authorization pointers SHOULD include expiration, revocation, or policy URLs when available.

## 6. Arabic Summary | ملخص عربي

OpenIdentity هو ملف هوية محمول لوكلاء الذكاء الاصطناعي. يجمع الهوية، التحقق البشري، الأدوار، المهارات، أدوات MCP، بيانات A2A، روابط اكتشاف الذاكرة، مراجع المحافظ، ومؤشرات التفويض في ملف واحد آمن وقابل للمشاركة.
