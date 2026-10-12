# Param Chawla’s Network Lab

A responsive, static networking workspace built for Param Chawla, with interactive tools, original study content and a personal visual identity.

## Project structure

The `dist/` folder is the entire publishable website. It works on GitHub Pages without a framework, build service or database.

- `index.html`: application shell, identity and metadata.
- `workshop.js`: dashboard, learning paths, RF budget, IPv6 NDP, QoS, capture investigation and automation planner.
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

The lab includes 92 sidebar destinations. Several destinations share the same underlying lab (for example the BGP best-path selectors, ASN references and prefix policy builders).

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


## Workshop redesign

Local review version: ivory/charcoal palette, orange accents, serif headings, learning-path navigation and collapsed topic groups. Five new interactive topic pages supplement the original tools. RF and QoS use simplified models; capture cases are synthetic; automation exports local change plans without connecting to devices. Source syntax, core arithmetic and simulated DOM rendering checks passed. Browser visual validation remains incomplete because the loopback preview connection timed out.

## Repaired standalone preview

The standalone preview packaging now preserves all nine scripts exactly. Navigation audit: 86 pages passed; 79 initial control interactions passed; 92 deeper checks passed, including all 34 course modules and quiz progression. These checks use a DOM test environment. Visual browser testing remains incomplete because the loopback connection timed out and file navigation is blocked by browser policy.

## Wireless workbench

Added full-band 802.11ax MCS 0–11 rates (20/40/80/160 MHz, 1–8 spatial streams, 0.8/1.6/3.2 µs GI), a dedicated FSPL calculator, RF power/EIRP, payload-only airtime, first-Fresnel-zone clearance and 20 original lessons across CWNA/CWAP/CWDP/CWSP/CWNE. Lessons link to official CWNP resources and do not reproduce official courseware or exam questions. MCS is PHY rate, not throughput. All RF tools state their model limits.

About Param links the supplied LinkedIn profile; importing the About summary requires authenticated access or user-provided text. Attribution credits Chaithanya Kumar Katari and SubnetLab Pro, as requested.

Latest programmatic verification: 92 pages, 84 initial interactions and 114 detailed checks passed. MCS checks include 143.4 Mbps at 20 MHz/1SS/MCS11/GI0.8 and 1201.0 Mbps at 80 MHz/2SS; FSPL is 100.05 dB at 2.4 GHz/1 km. Visual browser verification remains incomplete.

## MCS explorer and CWNP practice update
The MCS explorer now computes Wi-Fi 4 HT (equal-modulation MCS 0–31, 1–4 streams), Wi-Fi 5 VHT (MCS 0–9, 1–4 streams), Wi-Fi 6/6E HE (0–11, 1–8 streams), and Wi-Fi 7 EHT (0–13, 1–8 streams). Widths and guard intervals follow the selected generation; unsupported VHT combinations display no rate. Full-band, unpunctured scope only. Includes search, rate calculation details, filtered CSV and print. SemFio Networks is credited as the interaction reference; rates are calculated locally.
Each of the 20 CWNP study modules opens its own wireless diagnostic scenario, with three answer choices, feedback, optional named calculation support and a return link to the originating lesson. No study practice button redirects to Automation Change Planner. These are original synthetic exercises, not live WLAN simulations or official exam questions.
Verification: all 20 lesson destinations and return links, 60 answer feedback paths, 3,279 rate/reference checks, search, filtered CSV and reset passed in a DOM harness. The full navigation audit rendered 93 pages; the two RIPE ASN lookup pages could not fetch their external service in the restricted test environment. Visual browser verification was unavailable. GitHub has not been updated with this local revision.

## Expanded free-space path-loss workbench
Added simultaneous 2.4/5/6 GHz comparison, channel and custom-frequency inputs, metre/feet conversion, loss/signal display, transmit power/gain/feeder budget, up to eight editable flat wall losses, linear/logarithmic SVG chart, reference-distance table, CSV and PNG chart export. Default frequencies match the SemFio reference (2437/5500/6195 MHz); that tool is credited. Loss is positive attenuation; estimated signal assumes 0 dBi receive gain. Exact speed-of-light formula rather than rounded constant. Model limits and channel-list limits appear beside the calculator.
Formula/reference and DOM interaction checks passed for default bands, distance doubling, EIRP, signal mode, unit consistency, wall boundaries/removal, chart scale, channel/custom frequency, CSV, validation and reset. The MCS/CWNP regression checks also passed. PNG export requires real browser canvas and remains visually unverified in this environment. Local update only; GitHub unchanged.

## Expanded CCNA / CCNP / CCIE courses
The course-content.js extension replaces short course cards with independently written deep dives, field/reference tables, worked calculations, per-module emulator walkthroughs, configuration/observation examples, expected results and diagnostic answers. CCNA now includes the original source's 16 topic areas plus four workshop extensions (20 total); CCNP has eight and CCIE ten. Attribution to Chaithanya Kumar Katari appears on each course. Guided device labs are external-emulator instructions, not claims of live browser device simulation or complete official blueprint coverage.
All 38 module lessons, 105 support/return links, 114 answer feedback paths, 38 exports, note/progress persistence and previous/next flows passed the DOM verification harness. Full 93-page audit and the wireless/FSPL regressions passed. See Network-Course-Comparison.md and network-lab-course-audit.json in the outputs folder. Visual local-browser verification remains unavailable. GitHub unchanged.
