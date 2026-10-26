# Store.link plugin for Claude, ChatGPT and Codex

Run your [Store.link](https://store.link) store from a conversation:

- "What sold this week?"
- "Mark order 10452 shipped and add the tracking number"
- "Add this product at $24 in Tees"
- "Make a 10% coupon that ends Sunday"
- "Write an About page"
- "Change the hero text"

The plugin connects your app to the Store.link connector at `https://dashboard.store.link/mcp` and adds a skill that teaches the assistant how a Store.link store works. You sign in with your Store.link account on first use. The assistant can do only what your role allows in each store.

## Install

### Claude Code

```
/plugin marketplace add microdotcompany/storelink-agent-plugin
/plugin install storelink@storelink
```

Then run `/mcp`, choose **storelink** and sign in.

### Codex

```
codex plugin marketplace add microdotcompany/storelink-agent-plugin
codex plugin add storelink@storelink
```

### claude.ai, Claude Desktop and ChatGPT

Add Store.link from the app's connector or plugin directory, or add a custom connector with the URL `https://dashboard.store.link/mcp`.

### Connector only

To connect without the skill:

```
claude mcp add --transport http storelink https://dashboard.store.link/mcp
codex mcp add storelink --url https://dashboard.store.link/mcp && codex mcp login storelink
```

## What it can do

- **Sales:** summaries, breakdowns (by product, day, coupon and more) and shipping times
- **Orders and customers:** look up orders and customers, update order status, add notes, take orders for customers
- **Products:** add and edit products, reorder categories, sync the Product Sheet
- **Coupons and pages:** create, change and delete
- **Design:** theme, colors, logo, menus and page sections
- **Settings:** store status and password, currency, language and storefront text, SEO, domains, shipping, the checkout form, where orders are sent, analytics, pixels, custom code, webhooks and team members

Payments, billing and plans, and creating, deleting or transferring a store stay in the [dashboard](https://dashboard.store.link).

Changes go live immediately. The assistant asks before emailing a customer or rebuilding your products from the Product Sheet.

## Disconnect

In the Store.link dashboard, go to Settings → Integrations → AI agents and click **Disconnect** next to the app.

## Support

[store.link/help](https://store.link/help/) · [Contact us](https://store.link/help/contact) · [Privacy](https://store.link/privacy) · [Terms](https://store.link/terms)

## License

MIT
