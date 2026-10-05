# Param Chawla’s Network Lab

A responsive, static networking workspace built for Param Chawla, with interactive tools, original study content and a personal visual identity.

## Project structure

The `dist/` folder is the entire publishable website. It works on GitHub Pages without a framework, build service or database.

- `index.html`: application shell, identity and metadata.
- `style.css`: responsive dark/light theme and print layout.
- `core.js`: addressing, aggregation, IPv6 and routing calculations.
- `data.js`: sidebar destinations, scenario data and question bank.
- `modules.js`: calculators, utilities and protocol playback.
- `protocol-view.js`: packet fields, TCP state transitions and routed packet tracing.
- `routing.js`: policy builders, topology, routing and analysis labs.
- `learning.js`: courses, quizzes, flashcards and troubleshooting.
- `webmcp.js`: optional browser agent integration, feature detected.

`serve.cjs` runs a local preview with `node serve.cjs` at `http://127.0.0.1:4173`.

## Scope

The lab includes 80 sidebar destinations. Several destinations share the same underlying lab (for example the BGP best-path selectors, ASN references and prefix policy builders).

The lab includes IPv4 and IPv6 tools, subnet splitting/joining, VLSM, overlap detection, exact and covering summaries, local password/X25519 generation, MAC conversion, ten unit calculators, simulated latency, RIPE Stat lookup, port reference, protocol timelines, ACL/prefix builders, OSPF SPF topology, STP and DR elections, LSA/area exploration, BGP attributes/policy, packet header decoding, show-output interpretation, routing-table parsing, convergence estimates, 15 broken-config challenges, a design interview, 24 questions, flashcards, and 34 course modules.

## Intended limits

- This is a teaching lab rather than an equipment emulator. Timeline scenes and latency are simulations; they do not send actual packets.
- Courses are concise original study modules with related hands-on tasks rather than official Cisco training.
- The OSPF topology editor models one area, bidirectional links and shortest paths. It uses an editable diagram/table with link costs and failure controls. Device configuration plans require operator adaptation.
- The packet decoder handles Ethernet, VLAN, IPv4 and common transport/control headers. It does not decode every DHCP option or validate checksums.
- The operational-output interpreter uses supported patterns rather than claiming to understand arbitrary vendor formats.
- Key generation needs a secure context and a browser with X25519 Web Crypto support. Passwords and private keys are not sent anywhere by the application. The passphrase dictionary is deliberately compact for learning.
- Only the explicitly triggered ASN/IP lookup accesses an external data service (RIPE Stat). It can fail if the network or service is unavailable.
- Native WebMCP browser validation was unavailable in the inspected browser. The optional registration/schema and execute contract are checked with a mock supporting context.

## Validation

Every sidebar destination was opened in the running browser without an application error. Core arithmetic checks cover `/0`, `/31`, `/32`, invalid inputs, VLSM capacity, overlap, exact summaries, IPv6 normalization, MAC parsing, BGP next-hop eligibility, and shortest paths with failed links. Representative browser interactions cover subnet split/join, VLSM, ACL first-match/implicit-deny behavior, protocol stepping and X25519 generation.

## GitHub Pages

Repository: https://github.com/Half-Duplex-Life/param-chawla-network-lab

The supplied workflow publishes `dist/` when pushed to `main` or run manually. In repository Settings → Pages, choose GitHub Actions as the publishing source. All asset references are relative, so both account-root and project Pages URLs work.

## Ownership

Branding identifies Param Chawla as the lab owner. No employment history, certificates, social profiles or contact details were invented or copied. The About panel links authoritative protocol documents.

