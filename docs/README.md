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
| `SITE_DECISION.md` | Site-lokal design- og implementeringsbaseline, inkl. SITE-###-beslutninger og SITE-007 Public Disclosure Boundary | ACTIVE WHEN PRESENT ON `main` | Site-local authority on `main`; candidate material elsewhere | Før enhver site-endring, og alltid før en SITE-###-post refereres | Noen endring av offentlig nettside — SITE-006 forblir NOT PASSED |
| `docs/SITE_WORKING_MODEL.md` | Arbeidsavtale for Jakob, ChatGPT, Claude Code og GitHub, inkl. Lifecycle Integrity og Public Disclosure Integrity Guards | ACTIVE WHEN PRESENT ON `main` | Workflow authority on `main`; candidate material elsewhere | Før en ny oppgave startes, og ved uklarhet om roller/rekkefølge | Endring av produkt, arkitektur eller offentlig nettside |
| `docs/README.md` (dette dokumentet) | Kompakt dokumentkart og lesehenvisning | ACTIVE NAVIGATOR WHEN PRESENT ON `main` | None | Ved oppstart av en oppgave, for å finne riktig dokument | Noe som helst — dette er kun en henvisning |
| `.github/pull_request_template.md` | Evidensbasert PR-mal | ACTIVE PROCESS TEMPLATE WHEN PRESENT ON `main` | Process only | Ved åpning av enhver PR mot denne repoen | Merge uten Founder-godkjenning |

## Anbefalt leserekkefølge

1. `SITE_DECISION.md`
2. `docs/SITE_WORKING_MODEL.md`
3. Gjeldende `main/index.html` — godkjent kilde for neste deploy
4. Applicable private Jakjo Product Truth, claim, IP and architecture
   authority — kun når ekstern tekst er involvert
5. Aktiv issue/PR for den konkrete oppgaven

## Definisjon: offentlig sannhet

Verifisert live deploy på vardeark.no er faktisk offentlig tilstand.

Dette kartet skiller mellom tre nivåer, som ikke må forveksles:

- **Branch/PR** = public candidate material. Ingen active authority,
  men umiddelbar public exposure fra push-tidspunktet (jf. SITE-007).
- **`main`** = approved public source for next deploy. Ikke i seg selv
  bevis på live website state.
- **Verified deploy** = faktisk public website state på
  `vardeark.no`.

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

## Repository visibility

Dette repositoryet er public.

Branches og PR-er er ikke private. Comment, review, issue og
attachment er heller ikke private staging surfaces. Alt som pushes
eller skrives til en public GitHub surface skal allerede være
public-safe og ha bestått Public Disclosure Integrity Guard før
handlingen utføres — guarden gjelder umiddelbart før hver public
write, ikke bare før første push.

Hele public artifact set kontrolleres i tillegg samlet før
ready-for-review og før merge.

Uavklart eller sensitivt materiale skal behandles lokalt eller i et
eksplisitt private workspace.
