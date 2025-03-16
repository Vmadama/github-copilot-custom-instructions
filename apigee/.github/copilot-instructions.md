# instructions.md

## Apigee Edge Policy Naming Conventions

This document defines naming conventions for policies in Apigee Edge to ensure consistency and clarity.

### General Guidelines
- Use the full policy type name as the prefix (see table below).
- Follow the prefix with a hyphen (`-`) and a brief, meaningful description.
- Use hyphens (`-`) to separate words in names (e.g., `AssignMessage-set-headers`).
- Keep names concise but descriptive (max 30 characters recommended, though full prefixes may exceed this).
- Use numerical suffixes (e.g., `-01`, `-02`) for multiple similar policies.

### Policy Type Prefixes
| Policy Type          | Prefix           | Example                        |
|----------------------|------------------|--------------------------------|
| AssignMessage        | `AssignMessage`  | `AssignMessage-set-headers`    |
| JavaScript           | `JavaScript`     | `JavaScript-validate-input`    |
| ExtractVariables     | `ExtractVariables`| `ExtractVariables-parse-query`|
| ServiceCallout       | `ServiceCallout` | `ServiceCallout-call-external` |
| KeyValueMapOperations| `KeyValueMapOperations` | `KeyValueMapOperations-store-config` |
| RaiseFault           | `RaiseFault`     | `RaiseFault-raise-error`       |
| VerifyAPIKey         | `VerifyAPIKey`   | `VerifyAPIKey-check-key`       |
| OAuthV2              | `OAuthV2`        | `OAuthV2-generate-token`       |
| FlowCallout          | `FlowCallout`    | `FlowCallout-log-event`        |

### Examples
- `AssignMessage-set-headers` - Adds headers to a response.
- `JavaScript-validate-input-01` - First policy to validate input.
- `ExtractVariables-parse-query` - Parses query parameters.
- `ServiceCallout-call-external` - Calls an external service.
- `KeyValueMapOperations-store-config` - Stores config in KVM.
- `RaiseFault-raise-error` - Raises an error for invalid requests.
- `VerifyAPIKey-check-key` - Verifies an API key.
- `OAuthV2-generate-token` - Generates an OAuth token.
- `FlowCallout-log-event` - Logs an event.

### Notes
- Suffixes like `-01`, `-02` indicate execution order (e.g., `JavaScript-validate-input-01`).
- Names should reflect the policy’s purpose in the proxy flow.
- Note: Some names may exceed 30 characters due to full prefixes; adjust descriptions to shorten if needed.
