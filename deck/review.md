# Deck review: 7.8 / 10

Reviewer: subagent
Build: `1301504c1c2a6276` · 2026-10-21T16:23:19

Clear, honest seven-minute story: three energy topics under GMP, each ending in a concrete decision, and the formulas checked against Eurovent 4/24 and the choked-flow source (Eq. 3, Eq. 1, 1.89, R = 287 and Psi = 0.685 all verify). The weakest part is the evidence behind the results: the eco-mode gain is not shown even as a ratio, the leak bench never shows its calibration curve, slide 4 does not say how the candidate filter's replacement threshold is set (the figure's gain depends on it), and the 3 billion tablets source, Ward-Smith and the internal audit could not be opened.

| Gate | Count |
|---|---|
| failed source checks | 0 |
| unsourced numbers | 0 |
| images without credit/licence | 0 |
| image problems | 0 |

## Slides, lowest score first

### Slide 3: Mode éco des cabines de pesée : réduction du débit d'air neuf hors pesée (6.8)

message 7, evidence 4, honesty 7, legibility 8, consistency 7, timing 8

- [medium] The conclusion says the gain is sufficient to justify a regulation study, but the slide shows no number, ratio or method: the reader must take the claim on trust. **Fix:** Add a non-confidential indicator under the diagram, e.g. the gain as a percentage of the booth AHU's annual energy, or its split (thermal vs fan), plus the method line '1 an de supervision, ~N millions de lignes, Python'.
- [low] The AHU label says 'filtrer, chauffer, refroidir, sécher' but only three symbols are drawn (zigzag, box with diagonal, fan); no heating or cooling coil symbol is recognisable, and the zigzag reuses the filter symbol drawn on the exhaust. **Fix:** Draw separate filter, heating coil (+), cooling coil (-) and fan symbols, or label each box under the AHU.

### Slide 6: Application de traitement des relevés : débit et coût annuel par fuite (6.8)

message 6, evidence 4, honesty 6, legibility 8, consistency 8, timing 9

- [medium] The title promises 'débit et coût annuel par fuite', but the Terrain band says real leaks are below the bench domain: current field estimates are extrapolations, and the notes' 'résultats assez cohérents' has no evidence on the slide. **Fix:** Retitle e.g. 'Application : débit et coût estimés par fuite, calibration à étendre aux faibles débits' and add one line of field evidence (n fuites relevées, k hors plage calibrée).
- [low] Fluke's ii500 product page says the tool 'estimates relative leak size and cost' (LeakQ 1-10); a jury may ask why the app is needed. **Fix:** Add one phrase: 'la caméra ne donne qu'un indice relatif (LeakQ 1-10), pas de débit en L/min'.

### Slide 11: Mode éco : énergie annuelle pondérée par le temps de pesée (7.3)

message 7, evidence 5, honesty 7, legibility 8, consistency 8, timing 9

- [low] The slide cites the internal 2021 energy audit, but nothing on it says which input comes from the audit, and the audit is not public; how the fan electricity at reduced flow is obtained is not stated. **Fix:** Write 'P_max : audit énergétique 2021' (or whatever input it supplies) and add 'ventilateur à débit réduit : mesuré en supervision / lois de similitude'.

### Slide 2: Site pharmaceutique sous GMP : toute modification d'installation est soumise à validation (7.7)

message 6, evidence 6, honesty 7, legibility 9, consistency 9, timing 9

- [medium] The title claims the GMP validation constraint, but the dominant element is a group-level production figure (3 milliards) that does not support it; the constraint itself only appears in the title and the bottom 'Démarche' band. **Fix:** Shrink the 3 milliards stat to a secondary line and give the visual weight to the constraint, e.g. a short chain 'modification -> change control -> requalification' or 'toute modification = dossier de validation'.
- [medium] The cited source for 'plus de 3 milliards de comprimés par an' (pracodawcy.pracuj.pl) is behind a Cloudflare challenge and has no local copy, so it could not be checked; press reports give 3.2 to 3.5 billion depending on year. **Fix:** Save a PDF or screenshot of the pracuj.pl page in sources/ and set 'local', or cite a reachable dated source (e.g. the PAP article giving 3.5 mld tabletek rocznie) with its year.
- [low] 'GMP' is never expanded on the slides for a French jury. **Fix:** Write 'BPF / GMP (bonnes pratiques de fabrication)' the first time it appears.

### Slide 4: Filtres à faible perte de charge : perte de charge moyenne selon Eurovent 4/24 (7.7)

message 8, evidence 8, honesty 6, legibility 8, consistency 8, timing 8

- [medium] The candidate filter's threshold is drawn at 3 x its own initial pressure drop (1.8), not at the site's current threshold (3). The gain depends on this choice: with the same absolute threshold of 3, Eurovent Eq. (3) gives a candidate mean of (2x0.6+3)/3 = 1.4 instead of 1.0, which removes most of the shown gap. The slide does not say which rule applies. **Fix:** State the threshold rule on the slide ('seuil = 3 x Δp0, EN 13053' or 'seuil identique du site') and, if the site keeps a fixed final Δp, redraw the candidate with that threshold.
- [low] The x-axis runs to about 3.6 lifetimes but both curves stop at 2.6, and the current filter's third cycle is cut mid-cycle; Eurovent's lifetime-independent average holds only over full lifetime intervals. **Fix:** End the axis at 2.6 and stop the current filter at t = 2 (or extend both to a common full-cycle boundary, e.g. 3.9 = 3 x 1.3).
- [low] Y-axis 'rapportée à l'état neuf' does not say which filter's new state is the reference (the candidate starts at 0.6). **Fix:** Write 'rapportée à l'état neuf du filtre actuel'.

### Slide 5: Banc de référence : buse calibrée en écoulement critique (7.8)

message 7, evidence 6, honesty 7, legibility 9, consistency 9, timing 9

- [medium] The manometer is drawn upstream of the flexible hose, so it reads the pressure before the hose loss, not p0 at the nozzle inlet used in the critical-flow formula (R4); T0 is needed too but no temperature measurement is drawn. **Fix:** Move the gauge to just upstream of the nozzle (or state 'perte de charge du tuyau négligeable, vérifiée') and add a thermometer or the note 'T0 = température ambiante'.
- [medium] The bench's result (camera score/dB against computed flow, with its range) is never shown, although slide 6's estimates rest on it. **Fix:** Add a small calibration plot here: computed flow (L/min) vs dB and vs score, with the bench domain marked; it can carry masked costs but the flow axis is not confidential.
- [low] The slide cites Ward-Smith and Fluke in its data but shows no visible source line. **Fix:** Add 'Sources : Ward-Smith 1979 ; Fluke ii500' under the diagram.

### Slide 8: Bilan et enseignements (8.0)

message 8, evidence 6, honesty 8, legibility 9, consistency 9, timing 8

- [low] Right column has only two lessons and a large empty band; the strongest lesson in the notes ('aller voir l'installation avant de calculer') is not on the slide. **Fix:** Rephrase the first lesson as 'Aller voir l'installation avant de calculer : 1 à 2 semaines perdues sur les filtres'.

### Slide 10: Cascade de pression : l'air s'écoule de la pression la plus haute vers la plus basse (8.0)

message 8, evidence 6, honesty 8, legibility 9, consistency 8, timing 9

- [low] Backup slide with no source for the pressure-cascade principle; the standard room's 'pression intermédiaire' is not placed relative to the corridor's 'pression de référence' and has no arrow. **Fix:** Add a source (e.g. EU GMP Annex 1 or ASHRAE 170) and either draw a small arrow or write 'pression ≈ couloir' for the standard room.

### Slide 7: Livrables et décisions associées (8.2)

message 8, evidence 6, honesty 8, legibility 9, consistency 9, timing 9

- [low] Statuses are assertions with no date or owner, so 'proposé' and 'à engager' read as open-ended. **Fix:** Add an owner or horizon to each status, e.g. 'essai pilote proposé, CTA X, T1 2027'.

### Slide 1: Évaluation d'économies d'énergie sur un site pharmaceutique sous contrainte GMP (8.3)

message 8, evidence 8, honesty 8, legibility 9, consistency 8, timing 9

- [low] Kicker reads 'STAGE M1' while the Formation cell reads 'M2 GDP, UGA' and the notes say 'je suis en M2'; a jury may read this as a contradiction. **Fix:** Write 'STAGE DE M1 (2025)' in the kicker or 'Formation : M2 GDP, UGA (stage réalisé en M1)' so the two levels are explained.
- [low] The aerial photo's licence is recorded as 'autorisation d'usage non documentée'; credit is present and the image matches the Pabianice production and logistics centre built by ALSTAL. **Fix:** Get a one-line written OK from Adamed communication (or link the Adamed/ALSTAL press page it comes from) and record it in sources.json.

### Slide 9: Références (8.3)

message 8, evidence 8, honesty 8, legibility 9, consistency 8, timing 9

- [low] Web references have no URL, Fluke has no access date, and 'Wikipédia, Choked flow' is the English Wikipedia; the source for R = 287 J/(kg·K) is not listed. **Fix:** Add the URLs and access dates (pracuj.pl, fluke.com, en.wikipedia.org/wiki/Choked_flow) and write 'Wikipedia (en)'.

### Slide 13: Banc : débit d'une buse en écoulement critique (8.3)

message 8, evidence 7, honesty 9, legibility 8, consistency 9, timing 9

- [low] C_d is attributed to Ward-Smith 1979 but its value, the nozzle diameter and the pressure range used are not given, so the bench flow cannot be reproduced from the slide. **Fix:** Add 'C_d = … (Ward-Smith 1979, buse d = … mm), p0 = … à … bar abs'.

### Slide 12: Filtres : perte de charge moyenne selon Eurovent 4/24 (8.7)

message 8, evidence 9, honesty 9, legibility 9, consistency 8, timing 9

- [low] The legend gives no unit for W, and the condition under which Eq. (3) applies (filter replaced at a fixed final Δp) is implicit. **Fix:** Add 'W : énergie annuelle (kWh/an)' and '(remplacement au seuil, méthode condition based)'.

## Not verified (source unreachable)

- Slide 2: Groupe Adamed : plus de 3 milliards de comprimés produits par an (adamed_pracuj)
- Slide 13: C_d : coefficient de décharge (Ward-Smith 1979) (ward_smith_1979)
- Slide 11: Inputs of the eco-mode energy model (audit énergétique 2021) (audit2021)
