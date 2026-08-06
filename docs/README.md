# Dokumentkart — Varde Ark website

Status: NAVIGATOR — IKKE GOVERNANCE-DUPLIKAT
Sist oppdatert: 2026-08-06

Dette er et kompakt kart over site-kontroll-dokumentene i denne
repoen. Det er en navigator, ikke en egen governance-kilde. Ved
motstrid mellom dette kartet og dokumentet det peker til, gjelder
alltid dokumentet det peker til.

## Dokumenttabell

| Dokument | Formål | Status | Authority | Les når | Autoriserer ikke |
|---|---|---|---|---|---|
| `SITE_DECISION.md` | Site-lokal design- og implementeringsbaseline, inkl. SITE-###-beslutninger | CANDIDATE — REVIEW REQUIRED — NOT ACTIVE | Site-local candidate authority only | Før enhver site-endring, og alltid før en SITE-###-post refereres | Aktivering av noen SITE-###-post, eller noen endring av offentlig nettside |
| `docs/SITE_WORKING_MODEL.md` | Arbeidsavtale for Jakob, ChatGPT, Claude Code og GitHub | ACTIVE WORKING AGREEMENT | Workflow authority only | Før en ny oppgave startes, og ved uklarhet om roller/rekkefølge | Endring av produkt, arkitektur eller offentlig nettside |
| `docs/README.md` (dette dokumentet) | Kompakt dokumentkart og lesehenvisning | NAVIGATOR | None | Ved oppstart av en oppgave, for å finne riktig dokument | Noe som helst — dette er kun en henvisning |
| `.github/pull_request_template.md` | Evidensbasert PR-mal | ACTIVE TEMPLATE | Process only | Ved åpning av enhver PR mot denne repoen | Merge uten Founder-godkjenning |

## Anbefalt leserekkefølge

1. `SITE_DECISION.md`
2. `docs/SITE_WORKING_MODEL.md`
3. Gjeldende `main/index.html` (faktisk offentlig tilstand)
4. Relevant Jakjo Product Truth og claim-grenser
   (`Lekaste/Jakjo` `governance/JAKJO_PRODUCT_TRUTH.md`,
   `governance/competitive_position/POSITIONING_BOUNDARIES.md`) —
   kun når ekstern tekst er involvert
5. Aktiv issue/PR for den konkrete oppgaven

## Definisjon: offentlig sannhet

Offentlig sannhet er kun det som er verifisert live-deployet på
`vardeark.no`. `main`-branch er godkjent kilde for neste deploy, men
er ikke i seg selv bevis på faktisk offentlig tilstand før deploy er
verifisert.

## Definisjon: kandidatmateriale

Kandidatmateriale er alt som er foreslått, dokumentert eller opprettet
i en branch, PR, draft eller Handoff, men som ikke er godkjent av
Founder og merget til `main`. Kandidatmateriale gir ingen rettighet
til å endre den offentlige nettsiden.

## Regel mot duplikatdokumentasjon

Det skal finnes ett kanonisk dokument per tema. Ikke opprett et nytt
dokument for et tema som allerede er dekket av `SITE_DECISION.md` eller
`docs/SITE_WORKING_MODEL.md`. Utvid eksisterende dokument i stedet.

## Regel for oppdatering av dette kartet

Dette kartet skal oppdateres i samme PR når et kanonisk
site-kontroll-dokument legges til, gis nytt navn, erstattes eller
fjernes. Kartet skal aldri henge etter den faktiske dokumentstrukturen.
