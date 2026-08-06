# SITE_DECISION

Formål: Site-lokal design- og implementeringsbaseline for Varde Ark.

Status: CANDIDATE — REVIEW REQUIRED — NOT ACTIVE

Authority:
Site-local candidate authority only.
No Jakjo runtime, architecture, product, legal, or claim authority.
Activation requires explicit Founder approval and controlled merge to main.

Dato: 2026-08-06

---

## 1. Purpose

Dette dokumentet er den site-lokale kandidat-baselinen for design,
informasjonsarkitektur, teknisk standard og endringsstyring for
Varde Ark-nettstedet (`Lekaste/Varde-Ark-site`).

Dokumentet gir ikke selv rett til å endre den offentlige nettsiden. Det
etablerer et sett med nummererte SITE-###-kandidatbeslutninger som må
godkjennes eksplisitt av Founder før de kan aktiveres, og som uansett
krever at Joint Website Change Gate (SITE-006) er bestått for den
konkrete, avgrensede endringen.

## 2. Scope

Gjelder kun `Lekaste/Varde-Ark-site` — det statiske, site-lokale
arbeidsoverflaten for Varde Ark sin offentlige nettside.

Gjelder ikke:
- Jakjo-produktet, Jakjo-motoren, eller noe repository under `Lekaste/Jakjo`;
- forretningsstrategi, markedsplan eller juridisk policy;
- infrastruktur utover det som kreves for å publisere en statisk side.

## 3. Authority and precedence

En Founder-beslutning kan autorisere en konkret endring, men endrer
ikke alene aktiv site-baseline. Aktiv baseline endres først når
beslutningen er implementert, kontrollert og merget til `main`. En
løs chat-uttalelse, et issue, en PR-kommentar, en Handoff eller en
branch blir aldri stille til aktiv baseline-autoritet.

Rekkefølge ved motstrid:

1. Gjeldende Jakjo-autoritet, for alt som angår Jakjo som produkt,
   identitet, krav, personvern, data, sikkerhet og IP
   (`Lekaste/Jakjo` `governance/ARCHITECTURE_DECISIONS.md`,
   `governance/JAKJO_PRODUCT_TRUTH.md`,
   `governance/competitive_position/POSITIONING_BOUNDARIES.md`).
2. Eksplisitt Founder-godkjente og kontrollert mergede site-beslutninger
   på `main`.
3. Aktive `SITE_DECISION.md`-poster på `main`.
4. Aktiv arbeidsmodell (`docs/SITE_WORKING_MODEL.md`) på `main`.
5. Navigasjonsdokumenter (`docs/README.md`) — ikke selvstendig
   autoritet.

Dette dokumentet har ingen autoritet over Jakjo-produktet, Jakjo sin
arkitektur, eller Jakjo sine claim-grenser og dupliserer ikke
Jakjo-governance. Dette dokumentet kan ikke overstyre, utvide eller
gjenskape den autoriteten.

## 4. Current live baseline

Bekreftet lest fra `main` ved base-commit `e42e4f6e0287efdf9b37bb6a0d26b705dc9e7cec`:

- `index.html`: én enkelt, statisk pre-launch-side. Semantisk HTML5,
  innebygd CSS (ingen ekstern stilarkfil, ingen JavaScript, ingen
  byggeverktøy, ingen sporing/analytics/skjema). Viser tittelen
  "Varde Ark" og statusteksten "Pre-launch". Støtter
  `prefers-reduced-motion` og `forced-colors`, samt safe-area-innhold via
  `env(safe-area-inset-*)`.
- `CNAME`: `vardeark.no`.
- `README.md`: énlinjes repository-tittel, ingen ytterligere innhold.
- Ingen GitHub Actions-workflows, ingen pakkefiler, ingen
  byggekonfigurasjon funnet i repoet.

Dette er den faktiske, verifiserte tilstanden på `main` på tidspunktet
for dette dokumentet, og er referansepunktet for all fremtidig
site-endring inntil en ny, godkjent baseline erstatter den.

## 5. Design direction

Kandidatretning: behold den minimalistiske, rolige visuelle
identiteten som allerede finnes på `main` (sentrert typografi, dempet
fargepalett, stillestående layout uten navigasjon eller innhold utover
tittel og status). Endringer i visuell retning skal være evolusjonære,
ikke en fullstendig redesign, med mindre Founder eksplisitt godkjenner
noe annet (jf. SITE-001).

## 6. Information architecture

Nettstedet er i dag én enkelt side uten navigasjon eller undersider.
Enhver fremtidig utvidelse av informasjonsarkitekturen (flere sider,
navigasjon, innholdsseksjoner) er en egen, avgrenset endring som krever
egen vurdering og egen passering av Joint Website Change Gate — den
forhåndsgodkjennes ikke av dette dokumentet.

## 7. Responsive and accessibility standard

- Mobil og desktop skal begge støttes fullt ut.
- Semantisk HTML-struktur, tastaturoperabilitet, synlig fokusmarkering
  og tilstrekkelig kontrast er obligatorisk, ikke valgfritt.
- `prefers-reduced-motion` skal respekteres for all animasjon.
- Safe-area-innhold (`env(safe-area-inset-*)`) skal bevares eller
  forbedres, aldri fjernes eller svekkes uten begrunnelse.
- Tilgjengelighet er del av Definition of Done (seksjon 11), ikke en
  etterfølgende forbedring.

## 8. Technical standard

- Statisk HTML og CSS som førstevalg. Semantisk markup foretrekkes
  fremfor generiske `div`/`span`-strukturer der et semantisk element
  finnes.
- Ingen rammeverk, byggepipeline, ekstern avhengighet, analytics,
  skjematjeneste eller JavaScript uten dokumentert behov og eksplisitt
  Founder-godkjenning.
- Infrastruktur skal stå i forhold til nettstedets faktiske funksjon —
  én statisk pre-launch/identitetsside.

## 9. Claim, privacy, data, security, and IP boundaries

- All ekstern tekst på nettstedet skal være konsistent med gjeldende
  Jakjo Product Truth og positioning boundaries
  (`Lekaste/Jakjo` `governance/JAKJO_PRODUCT_TRUTH.md` og
  `governance/competitive_position/POSITIONING_BOUNDARIES.md`).
- Ingen ubegrunnede påstander om compliance, juridisk status,
  markedsvalidering, kundevalidering, enterprise-readiness, ROI,
  patentstatus eller produksjonsmodenhet.
- Ingen produktidentitetsdrift i beskrivelser av Jakjo.
- Ingen publisering av konfidensiell, personlig, kandidat-, kunde-
  eller patentsensitiv informasjon på nettstedet.
- Dette dokumentet oppretter ingen ny claim-autoritet. Ved konflikt
  gjelder Jakjo-governance foran dette dokumentet for alt som handler
  om Jakjo som produkt eller selskap.

## 10. Change workflow

1. Endring foreslås og beskrives med omfang, evidens og
   tilbakerullingsplan.
2. Endring implementeres på én aktiv site-arbeidsgren
   (jf. SITE-005), med Handoff.
3. Joint Website Change Gate (SITE-006) må passeres eksplisitt av
   både Jakob og ChatGPT for den konkrete, avgrensede endringen før
   noen endring av den offentlige nettsideoverflaten kan skje.
4. Merge til `main` krever eksplisitt Founder-godkjenning.
5. Verifisert deploy er eneste bekreftelse på faktisk offentlig
   tilstand — ikke en PR, en branch, en Handoff eller en chat-uttalelse.

## 11. Definition of Done

En site-endring er ferdig når:

- Omfanget er avgrenset og dokumentert;
- endringen er testet på mobil og desktop;
- tilgjengelighet (tastatur, fokus, kontrast, reduced-motion) er
  verifisert, ikke antatt;
- claim-, privacy-, data- og IP-grensene i seksjon 9 er sjekket;
- en Handoff med evidens finnes;
- Joint Website Change Gate er eksplisitt passert for den konkrete
  endringen (kun relevant for endringer som faktisk berører den
  offentlige nettsideoverflaten);
- Founder har gitt eksplisitt godkjenning før merge.

## 12. Stable decision register

Alle beslutninger under er **CANDIDATE** i denne PR-en. Ingen av dem er
aktive. Aktivering krever egen, eksplisitt Founder-beslutning og
kontrollert merge til `main`.

### SITE-001 — Existing-page evolution

Status: CANDIDATE

- Bygg videre på gjeldende `main/index.html`.
- Ingen fullstendig redesign uten eksplisitt Founder-godkjenning.
- Behold den minimale, rolige visuelle retningen med mindre en senere
  godkjent beslutning endrer den.

### SITE-002 — Static-first and dependency-minimal

Status: CANDIDATE

- Foretrekk semantisk HTML og CSS.
- Ingen rammeverk, byggepipeline, ekstern avhengighet, analytics,
  skjematjeneste eller JavaScript uten dokumentert behov og eksplisitt
  godkjenning.
- Unngå infrastruktur som ikke står i forhold til nettstedets funksjon.

### SITE-003 — Responsive and accessible by default

Status: CANDIDATE

- Mobil og desktop er begge påkrevd.
- Bruk semantisk struktur, tastaturoperabilitet, synlig fokus,
  tilstrekkelig kontrast og støtte for redusert bevegelse.
- Behold eller forbedre safe-area-oppførsel.
- Tilgjengelighet er del av Definition of Done, ikke en senere
  forbedring.

### SITE-004 — Controlled external claims

Status: CANDIDATE

- Ekstern tekst skal forbli konsistent med gjeldende Jakjo Product
  Truth og positioning boundaries.
- Ingen ubegrunnede påstander om compliance, juridisk status,
  markedsvalidering, kundevalidering, enterprise-readiness, ROI,
  patentstatus eller produksjonsmodenhet.
- Ingen produktidentitetsdrift.
- Ingen publisering av konfidensiell, personlig, kandidat-, kunde-
  eller patentsensitiv informasjon.

### SITE-005 — One controlled work surface

Status: CANDIDATE

- Normalt skal kun én aktiv website-branch/PR eksistere om gangen.
- En andre aktiv website-branch krever eksplisitt Founder-godkjenning
  og dokumentert begrunnelse.
- GitHub branches og PR-er er selve branch-registeret; det opprettes
  ikke et separat branch-governance-dokument.
- Enhver endring skal ha omfang, evidens, tilbakerullingsplan og en
  Handoff.
- En branch, PR, draft, Handoff eller chat-uttalelse er ikke offentlig
  sannhet.
- `main` er godkjent kilde; verifisert deploy er faktisk offentlig
  tilstand.

### SITE-006 — Joint Website Change Gate

Status: CANDIDATE

- Ingen endring av den offentlige nettsideoverflaten kan skje før
  Jakob og ChatGPT begge eksplisitt har uttalt at evidensgrunnlaget og
  beslutningsgrunnlaget er tilstrekkelig for den konkrete, avgrensede
  endringen.
- Gaten er endringsspesifikk og gir ikke autorisasjon for senere
  endringer.
- Planlegging, et draft, en branch, en Handoff eller en kandidat
  SITE-###-beslutning passerer ikke gaten.
- Inntil gaten er passert er kun skrivebeskyttet analyse, kontrollert
  dokumentasjon, beslutningsforberedelse og evidensinnsamling tillatt.
- Usikkerhet betyr STOP.

**Denne PR-en dokumenterer at Joint Website Change Gate (SITE-006)
ikke er passert. Ingen endring av den offentlige nettsideoverflaten er
autorisert av dette dokumentet eller av denne PR-en.**

## 13. Supersession rule

En SITE-###-beslutning kan kun endres eller erstattes gjennom en ny,
eksplisitt Founder-godkjent commit til dette dokumentet, med
begrunnelse og oppdatert changelog-post (seksjon 14). Ingen stille
endring er tillatt. Ved motstrid mellom en SITE-###-post og en
Jakjo-governance-fil, gjelder Jakjo-governance for alt som angår
Jakjo som produkt eller selskap (jf. seksjon 3).

## 14. Changelog

| Dato | Endring | Status | Forfatter |
|---|---|---|---|
| 2026-08-06 | Opprettet dokument med SITE-001 til SITE-006 som candidate-beslutninger. Ingen aktivering. | CANDIDATE — REVIEW REQUIRED — NOT ACTIVE | Claude Code (SITE-001 baseline task) |
