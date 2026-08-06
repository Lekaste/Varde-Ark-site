# SITE_DECISION

Formål: Site-lokal design- og implementeringsbaseline for Varde Ark.

Status: ACTIVE WHEN PRESENT ON `main`

Authority:
Site-local authority when present on `main`.
Candidate material everywhere else.
No Jakjo runtime, architecture, product, legal, or claim authority.

Dato: 2026-08-06

---

## 1. Purpose

Dette dokumentet er den site-lokale baselinen for design,
informasjonsarkitektur, teknisk standard og endringsstyring for
Varde Ark-nettstedet (`Lekaste/Varde-Ark-site`).

SITE-001 til SITE-007 er Founder-godkjent for kontrollert aktivering
og har site-lokal autoritet bare når dette dokumentet er til stede på
`main`. På branch eller i PR er dokumentet kandidatmateriale.

Dette dokumentet gir ikke selv rett til å endre den offentlige
nettsiden. Joint Website Change Gate (SITE-006) må uansett være
bestått for den konkrete, avgrensede endringen før noen endring av
den offentlige nettsideoverflaten kan skje.

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

1. Applicable private Jakjo product, claim, IP and architecture
   authority, for alt som angår Jakjo som produkt, identitet, krav,
   personvern, data, sikkerhet og IP.
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

Gjeldende site-retning når dokumentet er aktivt på `main`: behold den minimalistiske, rolige visuelle
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

- All ekstern tekst på nettstedet skal være konsistent med applicable
  private Jakjo product, claim, IP and architecture authority.
- Ingen ubegrunnede påstander om compliance, juridisk status,
  markedsvalidering, kundevalidering, enterprise-readiness, ROI,
  patentstatus eller produksjonsmodenhet.
- Ingen produktidentitetsdrift i beskrivelser av Jakjo.
- Ingen publisering av konfidensiell, personlig, kandidat-, kunde-
  eller patentsensitiv informasjon på nettstedet.
- Dette dokumentet oppretter ingen ny claim-autoritet. Ved konflikt
  gjelder Jakjo-governance foran dette dokumentet for alt som handler
  om Jakjo som produkt eller selskap.
- Public communication skal tydelig forklare problem, product
  artifact, intended value, verified status og governance discipline.
- Public communication skal ikke avsløre reconstructive technical
  detail, non-public architecture, runtime internals, exact decision
  logic, rules, thresholds, patent application content, claim
  strategy, filing strategy, patent counsel communication eller trade
  secrets.
- Applicable private Jakjo authority styrer klassifisering og
  disclosure boundary (jf. SITE-007).
- En innsendt patentsøknad gjør ikke automatisk søknadsinnhold,
  claims, drawings, filing strategy eller tilgrensende trade secrets
  public-safe.
- Uklarhet betyr STOP.

## 10. Change workflow

1. Endring foreslås og beskrives med omfang, evidens og
   tilbakerullingsplan. Lokal branch creation og local drafting kan
   skje før public push.
2. Public Disclosure Integrity Guard (jf. SITE-007,
   `docs/SITE_WORKING_MODEL.md` §3.2) skal bestås umiddelbart før hver
   public write. Hele public artifact set skal i tillegg gjennomgås
   samlet på nytt før ready-for-review og før merge. Stage-specific
   kontroll:
   - Før push: branch name, filenames, diff og commit message.
   - Før PR creation eller update: PR title og PR body.
   - Før comment, review eller issue: den konkrete teksten og
     eventuell metadata.
   - Før upload, tag, release eller artifact publication: fil, navn,
     metadata og innhold.
   - Før ready-for-review og merge: hele public artifact set.
   En branch, commit, PR, comment, review eller issue skal aldri
   brukes som scratchpad for sensitivt eller uavklart materiale.
3. Endring implementeres på én aktiv site-arbeidsgren
   (jf. SITE-005), med Handoff.
4. Joint Website Change Gate (SITE-006) må passeres eksplisitt av
   både Jakob og ChatGPT for den konkrete, avgrensede endringen før
   noen endring av den offentlige nettsideoverflaten kan skje.
5. Merge til `main` krever eksplisitt Founder-godkjenning.
6. Verifisert deploy er eneste bekreftelse på faktisk offentlig
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
- Founder har gitt eksplisitt godkjenning før merge;
- Enhver lifecycle- eller authority-endring har bestått Lifecycle
  Integrity Guard i `docs/SITE_WORKING_MODEL.md`;
- Hver public write har bestått en stage-specific Public Disclosure
  Integrity review (jf. seksjon 10);
- Hele public artifact set har bestått samlet Public Disclosure
  Integrity review før ready-for-review og før merge. Public artifact
  set omfatter: filenames, file content, branch name, commit messages,
  PR title, PR body, comments, issues, attachments, samt genererte
  logs og artifacts.

## 12. Stable decision register

Alle beslutninger under er **ACTIVE WHEN PRESENT ON `main`**. Jf.
seksjon 3: en Founder-beslutning autoriserer, men aktiverer ikke alene
— aktivering skjer først når dette dokumentet er kontrollert merget
til `main`.

### SITE-001 — Existing-page evolution

Status: ACTIVE WHEN PRESENT ON `main`

- Bygg videre på gjeldende `main/index.html`.
- Ingen fullstendig redesign uten eksplisitt Founder-godkjenning.
- Behold den minimale, rolige visuelle retningen med mindre en senere
  godkjent beslutning endrer den.

### SITE-002 — Static-first and dependency-minimal

Status: ACTIVE WHEN PRESENT ON `main`

- Foretrekk semantisk HTML og CSS.
- Ingen rammeverk, byggepipeline, ekstern avhengighet, analytics,
  skjematjeneste eller JavaScript uten dokumentert behov og eksplisitt
  godkjenning.
- Unngå infrastruktur som ikke står i forhold til nettstedets funksjon.

### SITE-003 — Responsive and accessible by default

Status: ACTIVE WHEN PRESENT ON `main`

- Mobil og desktop er begge påkrevd.
- Bruk semantisk struktur, tastaturoperabilitet, synlig fokus,
  tilstrekkelig kontrast og støtte for redusert bevegelse.
- Behold eller forbedre safe-area-oppførsel.
- Tilgjengelighet er del av Definition of Done, ikke en senere
  forbedring.

### SITE-004 — Controlled external claims

Status: ACTIVE WHEN PRESENT ON `main`

- Ekstern tekst skal forbli konsistent med gjeldende Jakjo Product
  Truth og positioning boundaries.
- Ingen ubegrunnede påstander om compliance, juridisk status,
  markedsvalidering, kundevalidering, enterprise-readiness, ROI,
  patentstatus eller produksjonsmodenhet.
- Ingen produktidentitetsdrift.
- Ingen publisering av konfidensiell, personlig, kandidat-, kunde-
  eller patentsensitiv informasjon.

### SITE-005 — One controlled work surface

Status: ACTIVE WHEN PRESENT ON `main`

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

Status: ACTIVE WHEN PRESENT ON `main`

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

### SITE-007 — Public Repository Disclosure Boundary

Status: ACTIVE WHEN PRESENT ON `main`

- Dette repositoryet er public. Alle branches, commits, PR-er,
  comments, issues, attachments, tags og andre pushed GitHub surfaces
  skal behandles som umiddelbar offentlig eksponering.
- Branches og PR-er er offentlig kandidatmateriale. De er ikke private
  staging areas og har ingen aktiv site-local authority før
  kontrollert merge til `main`.
- Public Disclosure Integrity Guard (`docs/SITE_WORKING_MODEL.md`
  §3.2) skal bestås umiddelbart før hver public write — push, PR
  creation/update, comment, review, issue, attachment, tag, release
  eller annen publisering til en public GitHub surface. Hele public
  artifact set skal i tillegg gjennomgås samlet på nytt før
  ready-for-review og før merge.
- Public artifact set omfatter også external session links, ephemeral
  tool identifiers, temporary workspace references og generated
  footers — disse skal ikke publiseres uten dokumentert nødvendighet.
- Uavklart eller sensitivt materiale skal behandles lokalt eller i et
  eksplisitt private workspace. Det skal aldri pushes hit for å bli
  vurdert i etterkant.
- Public communication skal forklare problem, product artifact,
  intended value, verified status og governance discipline tydelig og
  profesjonelt.
- Public communication skal ikke avsløre non-public implementation,
  reconstructive technical detail, runtime internals, exact decision
  logic, patent application content, claim strategy, patent counsel
  communication eller trade secrets.
- En innsendt patentsøknad gjør ikke automatisk teknisk innhold,
  claims, drawings, filing strategy eller tilgrensende trade secrets
  public-safe.
- Public classification:
  - GREEN: Public-safe og kan deles.
  - YELLOW: Krever eksplisitt Founder- og ChatGPT-clearance.
  - Patent-relevant YELLOW krever i tillegg clearance fra qualified
    patent counsel.
  - RED: Skal aldri pushes til dette repositoryet.
- Uklar klassifisering behandles som RED.
- Brudd, uklarhet eller manglende clearance gir:

```text
FAIL — PUBLIC DISCLOSURE INTEGRITY
```

- SITE-007 passerer ikke SITE-006. Public website changes krever
  fortsatt separat Joint Website Change Gate for den konkrete,
  avgrensede endringen.

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
| 2026-08-06 | Founder godkjente SITE-001-baselinen for kontrollert aktivering. Livssyklus justert til å bli aktiv kun ved tilstedeværelse på `main`. Ingen endring av den offentlige nettsiden ble autorisert. Joint Website Change Gate (SITE-006) forblir NOT PASSED. | ACTIVE WHEN PRESENT ON `main` | Claude Code (SITE-001 activation-prep task) |
| 2026-08-06 | Rettet motstridende candidate/active-semantikk funnet i endelig ChatGPT-governancegjennomgang (authority-blokk, formål og designretning refererte fortsatt til kandidat/venter-på-godkjenning-tilstand etter at livssyklusstatus var endret til aktiv). Ordlyd i authority, formål og designretning justert. Lifecycle Integrity Guard i `docs/SITE_WORKING_MODEL.md` referert. Ingen endring av den offentlige nettsiden ble autorisert. Joint Website Change Gate (SITE-006) forblir NOT PASSED. | ACTIVE WHEN PRESENT ON `main` | Claude Code (SITE-001 lifecycle-integrity task) |
| 2026-08-06 | Founder autoriserte SITE-007 (Public Repository Disclosure Boundary). Public branches og PR-er presisert som offentlig eksponering fra push-tidspunktet. Pre-push Public Disclosure Integrity Guard etablert (`docs/SITE_WORKING_MODEL.md` §3.2). Patent application- og trade-secret-grensen presisert. Konkrete private Jakjo governance-paths redusert til generisk henvisning i normative public sections. Ingen endring av den offentlige nettsiden ble autorisert. Joint Website Change Gate (SITE-006) forblir NOT PASSED. | ACTIVE WHEN PRESENT ON `main` | Claude Code (SITE-007 public-disclosure-gate task) |
| 2026-08-06 | Endelig ChatGPT-governancegjennomgang identifiserte et timing gap: pre-push/pre-merge-guarden dekket ikke eksplisitt public writes mellom disse tidspunktene (PR-body updates, comments, reviews, issues, attachments, logs, artifacts). Guarden styrket fra pre-push til pre-public-write, med stage-specific disclosure review for push, PR create/update, interaction og upload/publication, pluss samlet review før ready-for-review og merge. External session links, ephemeral tool identifiers og temporary workspace references lagt til i public artifact set-omfanget. Ingen kjent RED-lekkasje ble funnet. Ingen endring av den offentlige nettsiden ble autorisert. Joint Website Change Gate (SITE-006) forblir NOT PASSED. | ACTIVE WHEN PRESENT ON `main` | Claude Code (SITE-007 public-write-gate correction task) |
