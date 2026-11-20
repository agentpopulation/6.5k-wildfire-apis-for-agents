## Wildfire API endpoints, snapshot 15 Nov 2026

- 6,584 endpoints passed a keyless data call, tested 10–15 Nov 2026 (IST)
- 1,279 services · 40 country codes · 6,146 keyless JSON rows

### Download

- `Wildfire_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 6,584 rows, 319.9 kB gzipped (2.1 MB as CSV), SHA-256 `b092e9dc98fa0c278f2024723141374cd7e0e22a64cee56dacc82da7621dba04`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Wildfire_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Wildfire_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 2,986 · Wrap one layer query as a get_fire_layer tool: pass a place or bounding box, return the fire name, size, containment or danger class with a timeout.
- 📱 App features: 565 · Draw the fires near a user on a map: query a perimeter or incident layer with a bounding box (`geometry=` and `returnGeometry=true`), then shade the area by fire-danger rating.
- 🧠 Grounding and data pipelines: 1,288 · Load fire history and wildfire-risk layers on a schedule into your own store, so answers about the fire risk at a place cite a dated source and a layer name.
- 🧪 Evals and testing: 6,584 · Run your fire tool against a fixed set of URLs across formats; check that fire name, area, date or danger class parse, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release
- Left out: 135 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 2 layers marked editable in the title (they can hold entries that people added).
- Left out: 18 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 59 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 6 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 139 class-exercise copies of the same few wildfire layers in one ArcGIS Online organisation, many with a person's name in the title.
- Overlap: 141 of these URLs are also in 190k-weather-apis-for-agents.
- Overlap: 14 of these URLs are also in 270k-transit-apis-for-agents.
- Overlap: 80 of these URLs are also in 270k-water-apis-for-agents.
- Overlap: 8 of these URLs are also in 130k-finance-economy-apis-for-agents.
- Overlap: 2 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 85 of these URLs are also in 1.3m-government-open-data-apis.
- Overlap: 2 of these URLs are also in 290k-statistics-apis-for-agents.
- Overlap: 6 of these URLs are also in 86k-oceans-apis-for-agents.
- Overlap: 4 of these URLs are also in 24k-maritime-apis-for-agents.
- Overlap: 40 of these URLs are also in 170k-environment-apis-for-agents.
- Overlap: 15 of these URLs are also in 20k-air-quality-apis-for-agents.
- Overlap: 26 of these URLs are also in 380k-maps-gis-apis-for-agents.
- Overlap: 6,146 of these URLs are also in 2.5m-agent-ready-apis.
- Overlap: 152 of these URLs are also in 380k-science-apis-for-agents.
- Overlap: 6,246 of these URLs are also in 53k-hazards-apis-for-agents.
- Overlap: 1 of these URLs is also in 72k-energy-apis-for-agents.
- Overlap: 12 of these URLs are also in 25k-aviation-apis-for-agents.
- Overlap: 33 of these URLs are also in 10k-earthquake-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 10–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Wildfire API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
