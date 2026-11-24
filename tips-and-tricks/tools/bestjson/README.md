# BestJSON

Free browser-based tools for formatting, validating, previewing repairs and structurally comparing JSON. No account is required; tool input is processed locally. The hosted product is proprietary and the website includes analytics.

[Tools](https://bestjson.com/)

## Tip: preserve large identifiers

JavaScript Number cannot represent every integer above 9007199254740991. A parse/serialize cycle can silently change an identifier:

```javascript
JSON.stringify(JSON.parse('{"id":9007199254740993}'));
// '{"id":9007199254740992}'
```

When the API contract permits, store identifiers as JSON strings, for example `{"id":"9007199254740993"}`. Do not blindly quote amounts or counts that require numeric types. Check precision throughout parsing, formatting, export and downstream use.

[Further reading: Preserve Large Numbers and Identifiers in JSON](https://bestjson.com/learn/json-large-numbers)
