# auth.md

The Claude Usage Limit Official Table is a public, read-only reference dataset. No account or authentication is required to read the published data.

## Agent audience
AI agents and crawlers that read official Anthropic Claude plan usage limits.

## Registration / provisioning
This resource is fully public. There is no registration or credential issuance required to access the data. OAuth metadata below is published for compatibility with agent frameworks; the data endpoints remain open.

## OAuth discovery (compatibility)
- Authorization server metadata: [/.well-known/oauth-authorization-server](/.well-known/oauth-authorization-server)
- Protected resource metadata: [/.well-known/oauth-protected-resource](/.well-known/oauth-protected-resource)
- Issuer: https://usagecaptable.com
- Agent registration (`agent_auth`): advertised in the authorization server metadata above — `skill: oauth2`, `register_uri: https://usagecaptable.com/oauth/register`, with an `oauth2` method (`authorization_endpoint`, `token_endpoint`, `scopes: [read]`).

## agent_auth metadata
```json
{
  "skill": "oauth2",
  "register_uri": "https://usagecaptable.com/oauth/register",
  "methods": [
    {
      "type": "oauth2",
      "authorization_endpoint": "https://usagecaptable.com/oauth/authorize",
      "token_endpoint": "https://usagecaptable.com/oauth/token",
      "scopes": ["read"]
    }
  ]
}
```

## Notes
All limits are quoted from official Anthropic pricing and Claude help pages. "Not published" is preserved verbatim where Anthropic has not published a figure.
