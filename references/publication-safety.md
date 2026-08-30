# Publication safety

Apply this guide only when output is intended for public or external sharing, or when adding fixtures to this repository.

## Never publish

- credentials, tokens, cookies, private keys, or authentication material;
- private hosts, internal URLs, repository paths, branch names, or ticket identifiers;
- real employee or customer identities;
- confidential metrics, screenshots, logs, prompts, or proprietary schemas;
- copied internal documents, even when names are lightly replaced.

If suspected credentials appear, stop and ask for a redacted source. Do not reproduce the suspected value in the response.

## Build safe examples

- Use fictional organizations, components, and roles.
- Use reserved domains such as `example.com` or `example.invalid`.
- Use obviously synthetic identifiers and measurements.
- Change the scenario and data model, not only the nouns.
- State that the fixture is synthetic.

## Preserve private authoring

Sanitization is an explicit publication operation. When editing a private document for private use, preserve required internal technical identifiers unless the user asks to redact them. Flag exposure risk without silently changing semantics.
