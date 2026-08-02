# Redwood Materials

Redwood Materials is a Carson City, Nevada battery materials company founded in 2017 by former Tesla
CTO JB Straubel. It operates a domestic circular supply chain for lithium-ion batteries: collecting
and recycling end-of-life EV, consumer, micromobility and stationary-storage batteries, refining the
recovered lithium, nickel, cobalt and copper, and remanufacturing anode copper foil and cathode
active material for North American cell producers. Through Redwood Energy it also deploys second-life
battery energy storage systems for data centers and the grid.

## API surface

**None public.** As of 2026-08-02 Redwood Materials publishes no OpenAPI or Swagger definition, no
GraphQL endpoint, no MCP server, no A2A agent card, no AsyncAPI or documented webhook surface, no
SDK on any public package registry, and no developer portal or API reference.

The only machine-facing surface is the gated partner portal at `portal.redwoodmaterials.com`, where
automotive dismantlers and OEM dealers price and sell end-of-life EV and hybrid battery packs. It
authenticates through AWS Cognito and is backed by a private, Cognito-authorized AWS API Gateway
endpoint (`/api/cp`) that returns `403 Missing Authentication Token` anonymously. That backend is
undocumented and not offered to third parties, so it is deliberately not catalogued as an API.

The full negative discovery sweep — every host, path, subdomain and registry checked — is recorded
in [`well-known/redwood-materials-well-known.yml`](well-known/redwood-materials-well-known.yml) so
re-runs are auditable.

## Artifacts

- [`apis.yml`](apis.yml) — APIs.json 0.20 company index
- [`security/redwood-materials-domain-security.yml`](security/redwood-materials-domain-security.yml) — probed TLS, HSTS, DNSSEC, CAA, SPF, DMARC
- [`well-known/redwood-materials-well-known.yml`](well-known/redwood-materials-well-known.yml) — well-known + contract-discovery probe record
- [`llms/redwood-materials-llms.txt`](llms/redwood-materials-llms.txt) — generated llms.txt company profile

## Links

- Website — https://www.redwoodmaterials.com/
- About — https://www.redwoodmaterials.com/about/
- News — https://www.redwoodmaterials.com/news/
- Partner with us — https://www.redwoodmaterials.com/partner-with-us/
- Partner portal (login) — https://portal.redwoodmaterials.com/
- Careers — https://www.redwoodmaterials.com/join/
- GitHub — https://github.com/redwoodmaterials
- Secondary market — https://forgeglobal.com/redwood-materials_stock/
