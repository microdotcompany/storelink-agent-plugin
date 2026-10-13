# Store.link plugin for Claude, ChatGPT and Codex

Run your [Store.link](https://store.link) store from a conversation:

- "What sold this week?"
- "Mark order 10452 shipped and add the tracking number"
- "Add this product at $24 in Tees"
- "Make a 10% coupon that ends Sunday"
- "Write an About page"
- "Change the hero text"

The plugin connects your app to the Store.link connector at `https://dashboard.store.link/mcp` and adds a skill that teaches the assistant how a Store.link store works. You sign in with your Store.link account the first time you use it. The assistant can do what your role allows in each of your stores, and nothing else.

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

Read sales, orders, customers, products, coupons, pages and design; update order status and add order notes; take orders for customers; add and edit products; create, change and delete coupons and pages; change the storefront design and basic store settings.

Billing, store creation and deletion, domains, payment gateways, team members and custom code stay in the [dashboard](https://dashboard.store.link).

Changes go live on your storefront immediately. The assistant asks before anything that emails a customer.

## Disconnect

In the Store.link dashboard, go to Settings → Integrations → AI agents and click **Disconnect** next to the app.

## Support

[store.link/help](https://store.link/help/) · [Contact us](https://store.link/help/contact) · [Privacy](https://store.link/privacy) · [Terms](https://store.link/terms)

## License

MIT
