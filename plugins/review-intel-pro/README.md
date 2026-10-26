# Review Intel Pro for Claude

Review Intel Pro combines the `app-review-growth-analyzer` skill with the signed-in Review Intel connector. Give Claude an App Store or Google Play URL and, after you sign in, it can retrieve public written reviews before analysing them. If the connector is unavailable, upload or paste a Review Intel Markdown export and the same skill analyses the reviews you provide.

The connector is read-only. Its Pro access is decided by the hosted Review Intel service; this plugin does not include the service or change its access rules.

## Claude Code

In a Claude Code session, add this marketplace and then install the plugin:

```text
/plugin marketplace add angrysushi11/review-intelligence
/plugin install review-intel-pro@review-intel
```

Choose the installation scope when Claude Code asks. Start a new Claude Code session after installation so its skill and MCP configuration load. When you first use a Review Intel retrieval tool, complete the email-code sign-in in the browser it opens.

## Claude.ai and Claude Desktop

The remote connector can also be added directly to Claude. Anthropic's current instructions for Pro and Max users are:

1. Open **Settings > Connectors**.
2. In **Connectors**, choose **Add custom connector**.
3. Add this remote MCP server URL and choose **Add**:

   ```text
   https://www.willthiseverwork.com/review-intel/mcp
   ```

4. In a chat, open **Search and tools**, choose the connector, then select **Connect** to complete the Review Intel email-code sign-in.

On Team and Enterprise, an Owner or Primary Owner adds it from **Settings > Connectors > Organization connectors** first; each user then connects their own Review Intel account. Remote custom connectors require a supported paid Claude plan. Follow the same **Settings > Connectors** route in Claude Desktop; remote servers are not configured through `claude_desktop_config.json`.

## Use it

```text
Retrieve reviews from this App Store or Google Play URL and give me the first useful read.
```

You can instead upload or paste a Markdown review export and ask for a first read, a focused product, pricing, growth, ASO, support, trust, or competitor analysis.

## Links

- Product: <https://www.willthiseverwork.com/review-intel/>
- Privacy: <https://www.willthiseverwork.com/review-intel/privacy/>
- Terms: <https://www.willthiseverwork.com/review-intel/terms/>
- Support: <https://www.willthiseverwork.com/review-intel/support/>

## License

Apache License 2.0. See [LICENSE](./LICENSE).
