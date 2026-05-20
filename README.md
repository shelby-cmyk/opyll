# Opyll

Marketing site for Opyll — compounded GLP-1 + the Opyll Stack supplement system.

## Pages

- `index.html` — Homepage with hero, pricing, process, calculator, protocol, stack, FAQ
- `stack.html` — Full Stack product catalog (Core 4 + 9 specialty add-ons)
- `privacy.html` / `terms.html` / `hipaa.html` — Legal placeholders (counsel to finalize before launch)

## Assets

- `favicon.svg` — Opal-iridescent brand mark
- `og-image.svg` — Social share image
- `vial-sema.png` / `vial-tirz.png` — Compounded medication vials (placeholder color-shifts of RxPros base; replace before launch)
- `stack-rise.png` / `stack-daily.png` / `stack-hold.png` / `stack-flow.png` — Core 4 Stack product bottles

## Tech

Static HTML. No build step. Inline CSS + JS for speed.

## Tracking placeholders (replace before launch)

In the `<head>` of `index.html`:
- `EVERFLOW_TRACKING_DOMAIN` — Everflow tracking subdomain
- `EVERFLOW_OFFER_ID` — Opyll offer ID in Everflow
- `CLARITY_PROJECT_ID` — Microsoft Clarity project ID
- `GTM_CONTAINER_ID` — Google Tag Manager container ID

Page attribution helper exposed as `window.opyll`:
- `opyll.getParam(key)` — read persisted affiliate/UTM param
- `opyll.track(event, data)` — push to dataLayer; auto-fires Everflow conversion when `event === 'conversion'`

`data-track` and `data-track-loc` attributes are on every CTA for event measurement.

## Local preview

```bash
cd opyll-site
python3 -m http.server 4747
# open http://localhost:4747
```

## Pricing model (current)

- **Core (3-month plan)** — $149/mo sema, $199/mo tirz · billed upfront ($447 / $597)
- **Core (monthly)** — $199/mo sema, $249/mo tirz · pay-as-you-go
- **Complete** — Core + Opyll Stack — $228/mo (sema, 3-month) / $278/mo (tirz, 3-month)
- **Stack a la carte** — Individual SKUs $22-48/mo

## Placeholder content to swap before launch

- [ ] Vial PNGs — currently color-shifted RxPros placeholders, replace with originals or AI-generated renders
- [ ] Real Everflow / Clarity / GTM IDs
- [ ] Real assessment funnel (currently `#pricing` anchor scroll)
- [ ] Privacy / Terms / HIPAA Notice — full legal copy from counsel
- [ ] About / Science / Press pages (footer placeholder links)
