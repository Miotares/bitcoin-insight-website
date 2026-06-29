# Screenshot shot list

The homepage currently ships with **real screenshots where they still match the app**, plus
**polished CSS mockups** as interim visuals for the three new feature sections (Explore, Charts,
Security). Replace the mockups (and refresh the outdated shots) with real screenshots when ready.

**Style:** capture in the **same framed iPhone style** as the existing screenshots (device bezel
baked into the PNG, ~portrait). Drop the file into `/screenshots/` using the exact name below, the
page already points at it (or has a clearly-marked swap comment in `index.html`).

---

## 1) Refresh, these show the OLD 3-tab bar (Dashboard · Wallet · Settings)

The app now has **4 tabs** (Dashboard · Explore · Wallet · Settings) and a 24h price sparkline.
Anything where the bottom tab bar is visible should be re-shot.

| File | Capture | Used in |
| --- | --- | --- |
| `01-dashboard.png` | Dashboard top: live price **with the 24h sparkline**, block height, mempool, fees, hashrate, Moscow time, **4-tab bar** | Hero + carousel |
| `02-network.png` | Dashboard scrolled: Moscow time, circulating supply, halving, Lightning, fee distribution (4-tab bar) | Carousel |

> Detail screens (`03`–`07`, `09`, `10`) are pushed views without a tab bar and are still fine,
> re-shoot only if the data looks stale to you.

## 2) New, replace the interim CSS mockups (recommended)

| File | Capture | Replaces mockup in |
| --- | --- | --- |
| `11-explore.png` | **Explore tab**: search bar (“Block, transaction, or address”) + live “Latest Blocks” feed with the green live dot | `#explore` section |
| `14-chart-price.png` | **Price detail mid-scrub**: hero price, range picker (24H/1W/1M/1Y/All), area+line chart with the cursor dot + the value/date readout in the header | `#charts` section |
| `16-wallet-lock.png` | **Wallet locked screen**: Face ID prompt / “Unlock with Face ID” (optionally with a blurred balance behind) | `#security` section |

After adding any of these, open `index.html`, find the matching
`<!-- SCREENSHOT SLOT: replace this mockup ... -->` comment, and swap the `.device` mockup block for:

```html
<div class="screen-frame" style="width:264px">
  <img src="screenshots/11-explore.png" alt="Bitcoin Insight Explore tab with search and a live latest-blocks feed" width="264" height="571" loading="lazy">
</div>
```

## 3) Nice-to-have, extra carousel / future use

| File | Capture |
| --- | --- |
| `12-explore-block.png` | Block detail (height hero, stats grid, “Mined by” / financials) |
| `13-explore-tx.png` | Transaction detail (confirmation seal, fee rate, inputs/outputs) |
| `15-chart-fees.png` | Fees detail: 3-line Fast/Medium/Slow chart with legend |
| `17-wallet-hidden.png` | Wallet with balances blurred/hidden (privacy) |
| `18-settings-security.png` | Settings: “Require Face ID”, “Hide Balances”, “Gap Limit” |
| `19-paywall.png` | Widgets unlock / paywall sheet (one-time, no subscription) |
| `20-add-wallet-reject.png` | Add Wallet showing the “private key detected” rejection |

---

*Tip:* keep aspect ratio consistent (the carousel/section frames assume ~`width:height = 264:571`).
If you provide frameless screenshots instead, tell me and I'll switch the page to a CSS device frame.
