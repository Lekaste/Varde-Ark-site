# Dokumentkart — Varde Ark website

Status: ACTIVE NAVIGATOR WHEN PRESENT ON `main`
Authority: NONE — NAVIGATION ONLY
Sist oppdatert: 2026-08-06

Dette er et kompakt kart over site-kontroll-dokumentene i denne
repoen. Det er en navigator, ikke en egen governance-kilde. Ved
motstrid mellom dette kartet og dokumentet det peker til, gjelder
alltid dokumentet det peker til.

## Dokumenttabell

| Dokument | Formål | Status | Authority | Les når | Autoriserer ikke |
|---|---|---|---|---|---|
| `SITE_DECISION.md` | Site-lokal design- og implementeringsbaseline, inkl. SITE-###-beslutninger | ACTIVE WHEN PRESENT ON `main` | Site-local authority on `main`; candidate material elsewhere | Før enhver site-endring, og alltid før en SITE-###-post refereres | Noen endring av offentlig nettside — SITE-006 forblir NOT PASSED |
| `docs/SITE_WORKING_MODEL.md` | Arbeidsavtale for Jakob, ChatGPT, Claude Code og GitHub | ACTIVE WHEN PRESENT ON `main` | Workflow authority on `main`; candidate material elsewhere | Før en ny oppgave startes, og ved uklarhet om roller/rekkefølge | Endring av produkt, arkitektur eller offentlig nettside |
| `docs/README.md` (dette dokumentet) | Kompakt dokumentkart og lesehenvisning | ACTIVE NAVIGATOR WHEN PRESENT ON `main` | None | Ved oppstart av en oppgave, for å finne riktig dokument | Noe som helst — dette er kun en henvisning |
| `.github/pull_request_template.md` | Evidensbasert PR-mal | ACTIVE PROCESS TEMPLATE WHEN PRESENT ON `main` | Process only | Ved åpning av enhver PR mot denne repoen | Merge uten Founder-godkjenning |

## Anbefalt leserekkefølge

1. `SITE_DECISION.md`
2. `docs/SITE_WORKING_MODEL.md`
3. Gjeldende `main/index.html` — godkjent kilde for neste deploy
4. Relevant Jakjo Product Truth og claim-grenser
   (`Lekaste/Jakjo` `governance/JAKJO_PRODUCT_TRUTH.md`,
   `governance/competitive_position/POSITIONING_BOUNDARIES.md`) —
   kun når ekstern tekst er involvert
5. Aktiv issue/PR for den konkrete oppgaven

## Definisjon: offentlig sannhet

Verifisert live deploy på vardeark.no er faktisk offentlig tilstand.

Dette kartet skiller mellom tre nivåer, som ikke må forveksles:

- **Branch/PR** = kandidatmateriale. Ingen rettighet, ingen sannhet.
- **`main`** = godkjent kilde for neste deploy. Ikke i seg selv bevis
  på faktisk offentlig tilstand.
- **Verifisert deploy** = faktisk offentlig tilstand på `vardeark.no`.

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
