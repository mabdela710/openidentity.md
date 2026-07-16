# OpenIdentity Manifest Example

```yaml
openidentity: "0.1"
agent:
  id: "did:web:example.com:agents:axiom-assistant"
  name: "Axiom Assistant"
  type: "ai-agent"
  version: "0.1.0"
  description: "An AI agent discoverable through OpenIdentity and AxiomID."
controller:
  human:
    name: "Example Controller"
    verification: "https://axiomid.app/u/example"
verification:
  domain: "https://example.com/.well-known/openidentity.md"
  axiom_id: "https://axiomid.app/u/example"
capabilities:
  roles:
    - "research"
    - "workflow-automation"
  skills:
    - "identity-discovery"
    - "memory-routing"
mcp_tools:
  - name: "memory-index"
    server: "https://example.com/mcp/memory"
    approval: "controller-approved"
a2a:
  protocol: "draft"
  endpoint: "https://example.com/a2a"
discovery:
  memory:
    - label: "approved-public-memory"
      uri: "https://example.com/memory/index.json"
      access: "public-read"
wallets:
  - type: "did"
    address: "did:web:example.com:agents:axiom-assistant"
authorization:
  policy: "https://example.com/policies/agent-access.json"
links:
  repository: "https://github.com/Moeabdelaziz007/AxiomID"
  profile: "https://axiomid.app/u/example"
```
