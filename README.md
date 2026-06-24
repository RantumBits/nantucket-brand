# nantucketbrand.com

Single-page holding site for Nantucket Brand, hosted on GitHub Pages. Plain HTML +
inline CSS — no build step. Replaces the prior parked/for-sale page and quietly
collects a waitlist for the future made-to-order, made-in-USA line.

> Firewalled from the data-studio brand: nothing here links *out* to Rantum/AddressIntel.
> The only founder reference is a subtle "by Andrew Maury" footer link (entity-graph
> disambiguation only).

## Go live
1. **Wire the waitlist:** create a free form endpoint (Formspree / Buttondown / Tally)
   and replace `YOUR_FORM_ID` in `index.html`. Until then the mailto fallback works.
2. **Create the repo + push** (e.g. `RantumBits/nantucket-brand`), `main` branch.
3. **Enable Pages:** repo Settings → Pages → Source = `main` / root.
4. **Custom domain:** set `nantucketbrand.com` (the `CNAME` file is already here) and
   tick "Enforce HTTPS" once the cert provisions.
5. **DNS** (important — the domain was on Afternic/for-sale nameservers, so DNS needs
   pointing at GitHub Pages). At your registrar, set:
   - **Apex `@` → four A records:** `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153` (and optionally the matching AAAA records).
   - **`www` → CNAME** to `rantumbits.github.io`.
   Remove the Afternic nameservers / parking. Propagation can take a few hours.
