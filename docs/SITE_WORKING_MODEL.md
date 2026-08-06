# SITE WORKING MODEL

Version: 1.1
Date: 2026-08-06
Status: CANDIDATE — REVIEW REQUIRED — NOT ACTIVE
Authority: Workflow authority only

Activation requires explicit Founder approval and controlled merge to
`main`.

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
