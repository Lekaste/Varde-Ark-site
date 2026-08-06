# SITE WORKING MODEL

Version: 1.4
Date: 2026-08-06
Status: ACTIVE WHEN PRESENT ON `main`
Authority: Workflow authority when present on `main`; candidate material elsewhere

This workflow model is active only when present on `main`.
Copies on a branch or in a PR are candidate material.

Dette dokumentet gir ingen produkt-, arkitektur-, juridisk- eller
claim-autoritet. Det regulerer kun arbeidsflyten mellom Jakob, ChatGPT,
Claude Code og GitHub for denne repoen (`Lekaste/Varde-Ark-site`).

## 1. Formål

Etablere én forutsigbar, revisjonsvennlig arbeidsflyt for endringer i
denne repoen, slik at Jakob kan uttrykke enkel intensjon uten å
gjenta etablerte standarder hver gang, samtidig som kontrollnivået
opprettholdes fullt ut.

## 2. Operating chain

```text
FOUNDER INTENT
→ ChatGPT control and complete task prompt
→ Claude Code implementation and testing
→ Handoff with evidence
→ ChatGPT independent verification
→ one Founder decision
→ merge
→ deploy and live verification
```

## 3. Regler

- Færre meldinger, ikke færre kontroller.
- Én aktiv oppgave, én aktiv website-branch og én Founder-beslutning
  om gangen.
- Jakob kan uttrykke enkel intensjon uten å gjenta etablerte
  standarder.
- ChatGPT leser sannhet, kompilerer oppgaven, gjennomgår evidens, og
  kan utfordre foreslåtte endringer.
- ChatGPT kan utfordre Jakob når en foreslått endring er i konflikt
  med autoritet, sikkerhet, tilgjengelighet, juridisk/claim-sikkerhet,
  revisjonsevne, designretning, eller skaper unødvendig kompleksitet.
- En utfordring skal forklare risikoen og gi det minste robuste
  alternativet.
- ChatGPT kan ikke stille overstyre Jakob.
- Claude Code er utførelse, ikke autoritet.
- GitHub registrerer implementeringsevidens.
- Ingen merge uten eksplisitt Founder-godkjenning.
- Ingen endring av den offentlige nettsideoverflaten før både Jakob og
  ChatGPT eksplisitt har passert Joint Website Change Gate (SITE-006)
  for den konkrete, avgrensede endringen.
- Endringer i arbeidsmodell og prompt er tillatt når Jakob ber om det.
- Forespurte endringer skal vurderes, versjoneres og logges.
- Ingen stille endringer.
- Fordi repositoryet er public, må content classification og
  disclosure review skje før første push. Branch eller draft PR er
  ikke et private review-rom.

## 3.1 Lifecycle Integrity Guard

1. Enhver lifecycle- eller authority-endring skal gjennomgås som én
   fullstendig semantisk tilstand, ikke som isolerte metadatafelter.
2. Gjennomgangen skal sammenligne:
   - Status
   - Authority
   - Purpose
   - normativ beskrivende tekst
   - decision register
   - document map
   - PR-mal
   - changelog
   - PR-body
3. Gyldig candidate-/kandidat-ordlyd er begrenset til:
   - branch/PR/draft/Handoff-kontekst;
   - eksplisitte definisjoner av kandidatmateriale;
   - historiske changelog-rader;
   - forklaringer om at et kandidat-artefakt ikke passerer SITE-006.
4. Stale candidate-ordlyd inni en active-on-main normativ setning er
   et brudd.
5. Stale active-ordlyd inni et rent kandidat-artefakt er et brudd.
6. Blandet eller uforklart lifecycle-semantikk gir:

```text
FAIL — LIFECYCLE INTEGRITY
```

7. Ingen ready-for-review, merge-anbefaling eller merge kan skje før
   bruddet er rettet og uavhengig verifisert.
8. Validering skal inkludere:
   - automatisert termsøk;
   - manuell klassifisering av hvert lifecycle-relatert treff;
   - Handoff-evidens som lister sjekkede termer og resultat.
9. Denne guarden krever ikke et nytt governance-dokument eller en ny
   avhengighet.

## 3.2 Public Disclosure Integrity Guard

Dette repositoryet er public. Guarden gjelder før første push og på
nytt før merge.

1. Guarden gjelder før første push og på nytt før merge.
2. Hele public artifact set skal vurderes samlet:
   - filenames
   - file content
   - branch name
   - commit messages
   - PR title og body
   - comments
   - reviews
   - issues
   - attachments
   - logs
   - generated artifacts
3. Klassifisering:
   - GREEN: Public-safe.
   - YELLOW: Krever eksplisitt Founder- og ChatGPT-clearance.
   - Patent-relevant YELLOW: Krever qualified patent counsel-clearance
     i tillegg.
   - RED: Blocked.
4. Uklarhet klassifiseres som RED.
5. Public-safe communication skal være tydelig om:
   - problem
   - product artifact
   - intended value
   - verified status
   - governance discipline
6. Følgende skal ikke pushes:
   - non-public technical implementation;
   - reconstructive architecture eller runtime detail;
   - exact decision logic, rules eller thresholds;
   - patent application content, claims, drawings eller filing
     strategy;
   - patent counsel communication;
   - trade secrets;
   - private credentials;
   - personal data;
   - customer data;
   - confidential material.
7. En innsendt patentsøknad opphever ikke guarden.
8. Public branch eller PR er kandidatmateriale med hensyn til
   authority, men offentlig med hensyn til exposure.
9. Failure state:

```text
FAIL — PUBLIC DISCLOSURE INTEGRITY
```

10. Ved failure:
    - ingen push av uklassifisert innhold;
    - ingen PR creation;
    - ingen ready-for-review;
    - ingen merge;
    - flytt vurdering og sensitivt materiale til local/private
      workspace.
11. Guarden skal være fail-fast og krever ikke et nytt
    governance-dokument eller en ny dependency.

## 4. Standard ChatGPT-statusheader

Ved oppstart av og underveis i en oppgave skal ChatGPT bruke følgende
statusheader:

```text
Live source:
Authority read:
Active task:
Applicable SITE-###:
Repository changes:
Founder decision:
```

## 5. Standard Handoff-navn

```text
HANDOFF_SITE-<ID>_<TASK>_COMPLETED.md
```

Eksempel: `HANDOFF_SITE-001_SITE_BASELINE_COMPLETED.md`

Handoff-filer skal normalt holdes utenfor det sporede repoet
(committes ikke til `Lekaste/Varde-Ark-site`), med mindre en aktiv
regel eksplisitt krever noe annet.

### Minimum Handoff-felter

- Origin
- Task
- Authority read
- Repository/path
- Base SHA
- Branch
- HEAD SHA
- Changed files
- Previous/new state
- Implementation decisions
- Tests
- Desktop/mobile
- Accessibility
- Claim/privacy/data/IP
- Deviations
- Gaps
- Rollback
- PR
- Recommended next decision
- Repository visibility
- Public artifact set reviewed
- GREEN/YELLOW/RED classification
- Patent/application/trade-secret check
- Public Disclosure Integrity result

## 6. Forhold til SITE_DECISION.md

Dette dokumentet regulerer arbeidsflyt (hvem gjør hva, i hvilken
rekkefølge). `SITE_DECISION.md` regulerer innhold og design-/tekniske
beslutninger for selve nettstedet. Ved motstrid om innhold og design
gjelder `SITE_DECISION.md`; ved motstrid om arbeidsflyt gjelder dette
dokumentet.

## 7. Versjonering av dette dokumentet

Endringer i dette dokumentet krever Jakobs forespørsel eller
eksplisitte godkjenning, skal versjoneres (increment i `Version:`) og
logges nedenfor. Ingen stille endring er tillatt.

### Changelog

| Versjon | Dato | Endring |
|---|---|---|
| 1.0 | 2026-08-06 | Første versjon av arbeidsmodellen, opprettet som del av SITE-001-baseline. |
| 1.1 | 2026-08-06 | Formaliserer Joint Website Change Gate (SITE-006) som forutsetning for enhver endring av den offentlige nettsideoverflaten. Formaliserer én aktiv website-branch som standard (SITE-005). Presiserer at status er CANDIDATE — REVIEW REQUIRED — NOT ACTIVE inntil eksplisitt Founder-godkjenning og kontrollert merge til `main`. Dette er versjonen som gjennomgås i PR #1. |
| 1.2 | 2026-08-06 | Founder godkjente kontrollert aktivering. Livssyklus er nå aktiv kun på `main`. Endringer av den offentlige nettsiden krever fortsatt at SITE-006 passeres separat. PR #1 forblir docs-only. |
| 1.3 | 2026-08-06 | Lifecycle-authority-inkonsistens funnet i endelig ChatGPT-governancegjennomgang (stale candidate-ordlyd bevart etter at status ble endret til aktiv). Lifecycle Integrity Guard (seksjon 3.1) innført. Semantisk helhetsvalidering er nå obligatorisk ved enhver lifecycle- eller authority-endring. Ingen endring av den offentlige nettsiden ble autorisert. PR #1 forblir docs-only. |
| 1.4 | 2026-08-06 | SITE-007 implementert. Public branch/PR-eksponering presisert (alt som pushes til dette public repositoryet er offentlig fra push-tidspunktet, uavhengig av authority-status). Pre-push disclosure review etablert gjennom Public Disclosure Integrity Guard (seksjon 3.2). Patent application- og trade-secret-grensen presisert. Konkrete private Jakjo governance-paths redusert i public documentation. Ingen website-surface change autorisert. SITE-006 forblir NOT PASSED. |
