# Coinugget Widgets

Free embeddable crypto widgets for any website or blog — live prices and chart signals. No API key, no sign-up.

**[Widget Builder & Live Preview → widget.coinugget.com](https://widget.coinugget.com)**

Pick a widget, set coin, exchange, size and colors, then click the code to copy it. The builder is available in 17 languages, and the copied code shows the widget in the language you picked.

---

## Widgets (13)

### Market widgets

| Widget | What it shows | File |
|---|---|---|
| **Major Markets** | Prices and 24h change for major coins plus global indices, gold and oil | `top-coins-bar.html` |
| **Price Action** | Coins with the biggest move vs. the previous candle (5m–1d) | `price-action.html` |
| **RSI Signals** | RSI overbought (≥70) and oversold (≤30) coins (5m–1d) | `rsi-signals.html` |
| **Top 10 Gainers** | 24h top 10 gainers with an RSI badge | `top-gainers.html` |
| **Regional Premium** | Bitcoin premium across 10 regions | `regional-premium.html` |
| **Derivatives** | 24h liquidations and long/short ratios | `derivatives.html` |

### Chart signal widgets

Signals are evaluated on **closed candles** for Binance, Bybit and MEXC (perpetual by default, spot with `m=spot`). Clicking a coin opens the same coin and timeframe in the free [Coinugget Pro Chart](https://coinugget.com/chart).

| Widget | What it shows | File |
|---|---|---|
| **Coin Signals** | Active signals for one coin on 15m · 1H · 4H · 1D · 1W | `coin-signals.html` |
| **Trend Check** | Price above/below EMA 25 / 50 / 200 per timeframe, plus RSI | `trend-check.html` |
| **Mini Chart** | Candles with EMA 25 / 50 and recent signal marks | `mini-chart.html` |
| **Signal Scanner** | Coins currently matching one signal you pick (46 signal types) | `signal-scanner.html` |
| **Signal Leaders** | Coins with the most bullish-side / bearish-side signals | `signal-leaders.html` |
| **Signal Pulse** | Bullish vs. bearish signal counts per signal group | `signal-pulse.html` |
| **New Signals Ticker** | One-line strip of signals that just fired (full width) | `signal-ticker.html` |

---

## Quick start

The easiest way is the [builder](https://widget.coinugget.com). It produces code like this:

```html
<div style="width:260px;max-width:100%">
<iframe src="https://widget.coinugget.com/coin-signals.html?bg=transparent&theme=auto&coin=ETH" loading="lazy" width="260" height="420" frameborder="0" scrolling="no" style="display:block;max-width:100%"></iframe>
<div style="text-align:right;margin-top:2px"><a href="https://coinugget.com?utm_source=widget&amp;utm_medium=embed&amp;utm_campaign=coin-signals&amp;utm_content=attribution" target="_blank" rel="nofollow noopener" style="font-size:10px;color:#64748b;text-decoration:none;font-family:sans-serif">coinugget.com</a></div>
</div>
```

Paste it into your page's HTML. That's it. The outer `div` keeps the widget and its link together and lets the widget shrink on narrow screens.

### URL parameters

| Parameter | Values | Example |
|---|---|---|
| `theme` | `auto` (follows the reader's light/dark setting), `dark`, `light` | `theme=auto` |
| `bg` | `transparent` or a hex color without `#` | `bg=transparent` |
| `accent`, `text`, `border` | hex colors without `#` | `accent=6d70f2` |
| `lang` | `en ko ja zh es pt fr de it nl ru tr ar hi id th vi` | `lang=ja` |
| `coin` | coin symbol (Coin Signals, Trend Check, Mini Chart) | `coin=SOL` |
| `ex`, `m` | `binance` / `bybit` / `mexc`, `perp` / `spot` (signal widgets) | `ex=bybit&m=spot` |
| `tf` | starting timeframe `15m` `1h` `4h` `1d` `1w` (Mini Chart: up to `1d`) | `tf=4h` |
| `signal` | signal id for Signal Scanner | `signal=sr_flip_support` |
| `tfs` | timeframe set for the ticker | `tfs=15m,1h,4h` |
| `limit` | number of coins in Signal Scanner (3–15) | `limit=10` |

### Dark mode toggle on your site

`theme=auto` already follows the reader's system setting. If your site switches light/dark with its own button, add this line once and the widgets will follow it:

```html
<script src="https://widget.coinugget.com/embed.js" defer></script>
```

---

## Install notes

- **WordPress**: add a *Custom HTML* block and paste the code. Saving an iframe needs the `unfiltered_html` capability (usually administrators). If the widget disappears after saving, ask your site admin.
- **Other site builders**: use their custom code or embed block. Some free plans don't allow iframes.
- **Phones**: keep the width at 300px or less. The default 260px fits phone screens. The ticker is always full width.
- **Platforms that don't allow iframes** (for example Medium, Substack, Naver Blog, Telegram, Discord, X, email): share a screenshot and a link instead. For Telegram and Discord there are free market panel bots: [coinugget.com/bots](https://coinugget.com/bots).
- Widgets run in their own iframe, so they don't change your page's code. Signal widgets pause updates while the reader's tab is hidden.

---

## Notes

- Signals describe chart patterns on closed candles. They are information, not investment advice.
- Prices can differ slightly from other exchanges.
- Free to embed today, no account needed. The Coinugget logo and link stay in the widget.

---

## Links

- **Widget Builder**: [widget.coinugget.com](https://widget.coinugget.com)
- **Pro Chart** (free): [coinugget.com/chart](https://coinugget.com/chart)
- **Telegram & Discord bots**: [coinugget.com/bots](https://coinugget.com/bots)
- **Main site**: [coinugget.com](https://coinugget.com)

---

## License

MIT — see [LICENSE](LICENSE). This repository contains documentation and embed examples. The widgets are served from widget.coinugget.com.
