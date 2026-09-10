# Session 3, Connectors

**Time:** 75 minutes
**Primitive:** MCP, the plug between Claude and your live systems
**Teammate upgraded:** 03, Voice of Customer, now on live data
**You walk out with:** Shopify, Drive and Gmail connected, and one report rebuilt on real numbers instead of a pasted file

---

## Before you start

- [ ] Sessions 1 and 2 done, both reports sitting in `my-work/`
- [ ] Admin access to your Shopify store, or whatever store platform you use
- [ ] The Google account your business actually runs on

---

## What this teaches

Everything so far read files you put in a folder. That has a ceiling: the moment your data changes, your reports are stale and you did not notice.

**MCP** is the standard that lets Claude talk to a live system. A connector is one of those, already packaged. Once Shopify is connected, a teammate does not read `products.csv`, it reads your actual catalogue, today, including the SKU you added this morning.

The difference shows up immediately in Session 9, where a weekly brief on a four month old spreadsheet is worse than no brief at all, because it reads just as confident.

---

## Steps

### 1. Connect a first-party connector

Click the **+** button next to the prompt box and choose **Connectors**.

You will see a list of services with built-in sign-in: Google Drive, Gmail, GitHub, Slack, Linear, Notion and others.

**Connect Google Drive.** Click it, sign in with your business Google account, approve the scopes it asks for. It should come back showing as connected.

**Then connect Gmail** the same way.

> **A word on scopes.** Read what you are approving. These connectors can read your documents and mail. That is the point, it is how a teammate finds your support threads. But approve them on the account you are comfortable with, and if you share this machine, use Manual permission mode for the rest of the session.

### 2. Connect your store

Shopify is not always in the first-party list, so it may need adding as a custom server.

**First check the Connectors list.** If Shopify is there, connect it the same way as Drive.

**If it is not there,** open the walkthrough at [`references/module-3-mcps/mcp-setup-shopify.md`](references/module-3-mcps/mcp-setup-shopify.md) and follow it. In short: a project-scoped MCP server is defined in a file called `.mcp.json` at the root of this repo, and the app picks it up when the project loads.

You can ask Claude to do it for you:

```
Add the Shopify MCP server to this project as a project-scoped server in .mcp.json, then tell me exactly what I need to authenticate and where I get it.
```

**Not on Shopify?** Use the sample data instead. `examples/d2c-marketplace-samples/` holds realistic Amazon and Flipkart exports, and `examples/the-paan-legacy/sample-inputs/` holds Shopify-shape CSVs. You will learn the same lesson one step removed.

### 3. Verify the connection points at the right place

**Do this before you trust a single number.** Type:

```
Which store am I connected to? Give me the store name, the domain and the currency.
```

If the answer is not your brand, stop. Every report built on that connection will be about somebody else's business, and it will look completely plausible. This is the single most common silent failure in this session.

### 4. Pull something real

```
Using the connected store, show me my top 10 products by orders over the last 30 days, with conversion rate and average rating for each.
```

Watch it request permission, call the connector, and answer. Compare the numbers against what you know. If they look wrong, the connection or the date window is wrong, and it is much cheaper to find that now.

### 5. Re-run Voice of Customer on live data

This is the payoff.

```
/voice-of-customer

Use the connected store for order and customer data, and search Gmail for customer support threads from the last 60 days. Cross-reference the themes against my product performance.
```

It will confirm the sources and the window before clustering. Say go.

**Compare it to Session 2's report.** The Session 2 version knew what customers said. This one knows what they said *and* what they then bought. That is the difference a connector buys you.

### 6. Point it at your nominated SKUs

If you filled `brand-brain/nominated-skus.md`, use it now:

```
Re-run the sentiment cut for only the five SKUs in brand-brain/nominated-skus.md, and tell me which of the five has the biggest gap between its rating and its conversion rate.
```

A high rating with a low conversion rate is a page problem, not a product problem. That finding is what Session 7 acts on.

---

## Check it worked

- [ ] Google Drive shows as connected
- [ ] Gmail shows as connected
- [ ] Your store is connected, **and you verified the store name out loud**
- [ ] You pulled live product data and sanity-checked it against what you know
- [ ] `my-work/voice-of-customer/` has a second, newer report that cites live data
- [ ] You can name one thing the live report found that the file-based one could not

---

## If it breaks

**The connector signs in but returns nothing.**
Usually scopes. Disconnect it, reconnect, and read the permission screen rather than clicking through. Drive in particular needs read access to the folders you care about.

**"I am connected to a store" but it is the wrong one.**
Disconnect and reconnect on the right account. Do not proceed. A confident report about the wrong business is the worst output in this whole bootcamp.

**Shopify will not connect at all.**
Do not burn the session on it. Export your products and orders to CSV from the Shopify admin, drop them in `brand-brain/`, and carry on. Every skill this weekend works from files. Fix the connection at home with [`references/module-3-mcps/mcp-setup-shopify.md`](references/module-3-mcps/mcp-setup-shopify.md).

**It keeps asking permission for the same thing.**
Choose "Always allow" on that tool, or switch to Accept edits mode.

**Gmail returns thousands of threads and the run stalls.**
Narrow it. Give it a date window and a search term: "support threads from the last 30 days mentioning delivery or refund".

---

## Take-home

Read [`references/module-3-mcps/mcp-setup-drive-gmail.md`](references/module-3-mcps/mcp-setup-drive-gmail.md) for what else Drive and Gmail unlock, and [`resources.md`](resources.md) for which connectors are worth adding next. Add them one at a time, and verify each one points at the right account before you trust it.

**Next:** [Session 4, Content Lead](session-4-content-lead.md)
