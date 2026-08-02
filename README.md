# Chobani

Chobani is an American food and beverage company founded in 2005 by Hamdi Ulukaya, best known for popularizing strained Greek yogurt in the United States and for operating what it describes as the world's largest yogurt facility in Twin Falls, Idaho. Its portfolio spans Greek yogurt, oat milk, plant-based yogurt, probiotic drinks, nutritional shakes, and — following the 2023 acquisition of La Colombe Coffee Roasters — ready-to-drink coffee.

- Website: https://www.chobani.com/
- About: https://www.chobani.com/about
- Newsroom: https://www.chobani.com/newsroom/our-news
- Careers: https://www.chobani.com/careers
- Consumer Care: https://chobaniconsumercare.powerappsportals.com/

## API surface

**Chobani publishes no public API.** Contract discovery on 2026-08-02 probed `www.chobani.com`, `chobani.com`, `api.chobani.com`, `shop.chobani.com` and the `developer.` / `developers.` / `docs.` / `status.` / `trust.` / `security.` / `partners.` subdomains for OpenAPI, Swagger, GraphQL, MCP, `llms.txt`, `security.txt` and A2A agent cards. Every canonical path returned 404 or NXDOMAIN.

- `api.chobani.com` resolves via Azure Front Door but serves an nginx 404 at the root and is undocumented.
- `shop.chobani.com` answers HTTP 200 for *every* path with the same Next.js HTML shell — those 200s were fetched, inspected, and rejected as single-page-app catch-all false positives (including `/.well-known/agent-card.json`).
- `chobani.com/robots.txt` discloses a first-party, `Disallow`-ed `/api/v1/*` backend that powers the website. It is undocumented, carries no published contract, and was not probed. It is not a public API.
- Trading-partner integration with Chobani runs over EDI, not an open API.

Full probe record with HTTP statuses: [`well-known/chobani-well-known.yml`](well-known/chobani-well-known.yml).

## Artifacts

| Artifact | File | Method |
|---|---|---|
| Discovery record | `well-known/chobani-well-known.yml` | probed |
| Domain security | `security/chobani-domain-security.yml` | probed |
| llms.txt | `llms/chobani-llms.txt` | generated |

Source: harvest backlog, secondary-market listing — https://www.hiive.com/securities/chobani-stock
