# Unkey

Unkey is the developer platform for modern APIs, providing globally distributed API key management, rate limiting, identity management, analytics, and deployment capabilities. The platform enables API providers to issue, verify, and revoke keys with metadata, expiration, usage credits, permissions, and roles — without managing any infrastructure.

**Website:** [unkey.com](https://www.unkey.com)
**Documentation:** [unkey.com/docs](https://www.unkey.com/docs)
**GitHub:** [github.com/unkeyed/unkey](https://github.com/unkeyed/unkey)

---

## APIs

### Unkey API (v2.0.0)

REST API providing programmatic access to all Unkey platform resources. Base URL: `https://api.unkey.com`

Authentication: Bearer token (root key) — `Authorization: Bearer unkey_xxx`

**Operations by resource group:**

| Group | Endpoints |
|---|---|
| **Keys** | create, verify, get, update, reroll, delete, whoami, add/remove/set permissions, add/remove/set roles, update credits, migrate |
| **APIs** | create, get, delete API namespace, list keys |
| **Identities** | create, get, update, delete, list |
| **Permissions** | create, get, delete, list |
| **Roles** | create, get, delete, list |
| **Rate Limits** | limit, multi-limit, set/get/list/delete overrides |
| **Analytics** | query key verification data via SQL |
| **Deploy** | create deployment, get deployment |
| **Liveness** | health check |

- [OpenAPI Specification](openapi/unkey-openapi.yml)

---

## Artifacts

### OpenAPI
| File | Description |
|---|---|
| [unkey-openapi.yml](openapi/unkey-openapi.yml) | Full Unkey API OpenAPI 3.1.0 specification (42 operations, 147 schemas) |

### Spectral Rules
| File | Description |
|---|---|
| [unkey-rules.yml](rules/unkey-rules.yml) | Spectral ruleset enforcing Unkey API conventions |

### Capabilities (Naftiko)
| File | Description |
|---|---|
| [shared/unkey.yaml](capabilities/shared/unkey.yaml) | Shared Unkey API consumed definition |
| [api-key-management.yaml](capabilities/api-key-management.yaml) | API key lifecycle workflow (14 tools) |
| [rate-limiting.yaml](capabilities/rate-limiting.yaml) | Rate limiting and override management workflow (6 tools) |
| [identity-management.yaml](capabilities/identity-management.yaml) | Identity lifecycle workflow (5 tools) |

### JSON Schema
| File | Description |
|---|---|
| [unkey-key-schema.json](json-schema/unkey-key-schema.json) | API Key entity schema |
| [unkey-ratelimit-schema.json](json-schema/unkey-ratelimit-schema.json) | Rate Limit result schema |
| [unkey-identity-schema.json](json-schema/unkey-identity-schema.json) | Identity entity schema |

### JSON Structure
| File | Description |
|---|---|
| [unkey-key-structure.json](json-structure/unkey-key-structure.json) | API Key field documentation |

### JSON-LD Context
| File | Description |
|---|---|
| [unkey-context.jsonld](json-ld/unkey-context.jsonld) | Linked data context for Unkey domain concepts |

### Examples
| File | Description |
|---|---|
| [unkey-create-key-example.json](examples/unkey-create-key-example.json) | Create API key request/response |
| [unkey-verify-key-example.json](examples/unkey-verify-key-example.json) | Verify API key request/response |
| [unkey-get-key-example.json](examples/unkey-get-key-example.json) | Get API key by ID request/response |
| [unkey-ratelimit-limit-example.json](examples/unkey-ratelimit-limit-example.json) | Apply rate limiting request/response |

### Vocabulary
| File | Description |
|---|---|
| [unkey-vocabulary.yml](vocabulary/unkey-vocabulary.yml) | Domain vocabulary for Unkey platform concepts |

---

## APIs Index

- [apis.yml](apis.yml)

---

*Maintained by [API Evangelist](https://apievangelist.com)*
