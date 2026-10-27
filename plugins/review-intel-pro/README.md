# Review Intel Pro for Claude

Review Intel Pro combines the `app-review-growth-analyzer` skill with the signed-in Review Intel connector. Give Claude an App Store or Google Play URL and, after you sign in, it can retrieve public written reviews before analysing them. If the connector is unavailable, upload or paste a Review Intel Markdown export and the same skill analyses the reviews you provide.

The connector is read-only. Its Pro access is decided by the hosted Review Intel service; this plugin does not include the service or change its access rules.

## Claude Code

In a Claude Code session, add this marketplace and then install the plugin:

```text
/plugin marketplace add willthiseverwork/review-intelligence
/plugin install review-intel-pro@review-intel
```

Choose the installation scope when Claude Code asks. Start a new Claude Code session after installation so its skill and MCP configuration load. When you first use a Review Intel retrieval tool, complete the email-code sign-in in the browser it opens.

## Claude.ai and Claude Desktop

Add the hosted service as a custom connector using [Anthropic's current instructions](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp):

1. Open **Customize > Connectors**, then **+ Add > Add custom connector**.
2. Name it **Review Intel Pro** and enter this remote MCP URL:

   ```text
   https://www.willthiseverwork.com/review-intel/mcp
   ```

3. Continue through the detected authentication settings. Select **Sign in now**, retain the detected OAuth client settings, and add the connector. Complete Review Intel's email-code sign-in when prompted.
4. In a conversation, use **+ > Connectors** to enable it.

For Team and Enterprise, an authorized administrator first adds it under **Organization settings > Connectors**, using **Add > Custom > Web**. Members then find it under **Customize > Connectors** and connect individually.

Anthropic supports custom connectors on Free, Pro, Max, Team and Enterprise; Free allows one. Review Intel Pro access is separately controlled by the Review Intel service. These remote connectors work on Claude web and Desktop.

## Use it

```text
Retrieve reviews from this App Store or Google Play URL and give me the first useful read.
```

You can instead upload or paste a Markdown review export and ask for a first read, a focused product, pricing, growth, ASO, support, trust, or competitor analysis.

## Links

- Product: <https://www.willthiseverwork.com/review-intel/?utm_source=github&utm_medium=referral&utm_content=pro_plugin_readme>
- Privacy: <https://www.willthiseverwork.com/review-intel/privacy/>
- Terms: <https://www.willthiseverwork.com/review-intel/terms/>
- Support: <https://www.willthiseverwork.com/review-intel/support/>

## License

Apache License 2.0. See [LICENSE](./LICENSE).
