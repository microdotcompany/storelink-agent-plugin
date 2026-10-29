# Store.link plugin for Claude, ChatGPT and Codex

[Store.link](https://store.link) turns a Google Sheet into an online store. This plugin lets you create and run that store from a conversation. Ask things like:

- "Create a store for my homemade candles"
- "Add this product at $24 in Tees"
- "Mark order 10452 shipped and add the tracking number"
- "What sold this week?"
- "Make a 10% coupon that ends Sunday"
- "Write an About page"
- "Change the hero text"

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

- **Start a store:** tell it what you sell and get a live store with its own link
- **Products:** add products, change prices and stock, hide what you're not selling
- **Orders and customers:** find orders, mark them shipped, add tracking, take orders that come in by phone or chat
- **Sales:** what sold, your best sellers and how fast you ship
- **Coupons and pages:** make discount codes, write About and FAQ pages
- **Design:** colors, logo, menus and homepage sections
- **Settings:** shipping, checkout, your domain, language, your team and more

Payments, billing and deleting a store stay in the [dashboard](https://dashboard.store.link).

## Disconnect

In the Store.link dashboard, open **AI agents** in the sidebar and click **Disconnect** next to the app.

## Support

[store.link/help](https://store.link/help/) · [Contact us](https://store.link/help/contact) · [Privacy](https://store.link/privacy) · [Terms](https://store.link/terms)

## License

MIT
