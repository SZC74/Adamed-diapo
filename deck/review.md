# Deck review: 7.7 / 10

Reviewer: subagent
Build: `6041e1a0a51ae327` · 2026-10-21T21:00:28

The deck is clear and well structured: each topic slide has a question, a method and a result, the schematics are clean, and the equations in the backup slides check out against Eurovent 4/24, the Wikipedia choked-flow article and a recomputation (Ψ ≈ 0,685, 1,2^3,5 ≈ 1,89, R ≈ 287). Its weakest point is evidence. Slides 3 and 6 claim results ('Oui', 'le principe marche sur le terrain') with no figure, and the speaker notes for slide 6 say the field leaks fell below the bench's calibrated range. The backup slide R1 shows hospital patient rooms in a pharmaceutical-plant talk, and the '3 milliards' source could not be opened.

| Gate | Count |
|---|---|
| failed source checks | 0 |
| unsourced numbers | 0 |
| images without credit/licence | 0 |
| image problems | 0 |

## Slides, lowest score first

### Slide 6: Application de traitement des relevés (6.5)

message 6, evidence 4, honesty 5, legibility 8, consistency 7, timing 9

- [medium] 'Le principe marche sur le terrain' is unsupported, and the notes partly contradict it: the real leaks were smaller than the bench range, so the field readings fell outside the calibrated laws. **Fix:** Replace with 'Sur le terrain, les fuites relevées sont sous la plage du banc : un rotamètre a été acheté pour étendre l'étalonnage aux petits débits', and add the number of leaks surveyed if available.
- [low] This is the only topic slide without a 'Question :' line, which breaks the question → method → result pattern of slides 3 to 5. **Fix:** Add 'Question : Comment traiter des dizaines de relevés sans ressaisie ?' under the title.

### Slide 3: Mode éco des cabines de pesée (6.7)

message 7, evidence 4, honesty 6, legibility 8, consistency 9, timing 6

- [medium] The result 'Oui. Le gain justifie...' has no number at all. The notes say the amounts stay internal, so the audience must take the conclusion on trust. **Fix:** Show a normalised result that leaks no amounts, e.g. 'gain ≈ X % de l'énergie annuelle des cabines, surtout thermique'. Or give an order of magnitude in MWh/an.
- [medium] Why the eco mode is unused (a site test showed the negative pressure briefly reversing at regime changes) is only in the notes, yet it is the reason the question exists. **Fix:** Add under the question: 'Mode existant mais inutilisé : la dépression s'inverse brièvement aux changements de régime'.
- [low] The notes run to 180 words in 80 s (about 135 words/min), which is tight for a 7-minute talk with only 15 s of slack. **Fix:** Cut the description of the glycol loop from the notes; the schematic already shows it.

### Slide 10: L'air s'écoule de la pression haute vers la basse (6.8)

message 6, evidence 6, honesty 7, legibility 9, consistency 4, timing 9

- [medium] The pressure-cascade backup shows two hospital patient rooms ('chambre', 'patient') fed by a pressurised corridor. The talk is about a pharmaceutical plant whose weighing booth is in negative pressure relative to its room (slide 3). The example is off-topic and invites the wrong question. **Fix:** Redraw with the site's own case: room (or corridor) at higher pressure → weighing booth in negative pressure, with the airflow through the open front as on slide 3.

### Slide 2: Un site GMP impose de valider toute modification d'installation (7.2)

message 6, evidence 5, honesty 6, legibility 9, consistency 9, timing 8

- [medium] The cited source (pracodawcy.pracuj.pl) could not be opened: Cloudflare blocks it. A PAP report (Polskie Radio) gives a newer figure of 3.5 billion tablets a year. 'Plus de 3 milliards' is therefore not wrong, but the large '3 milliards' understates it, and the source cannot be checked. **Fix:** Save a local copy or a screenshot of the pracuj.pl page in sources/. Or show '3,5 milliards de comprimés par an' and cite PAP/Polskie Radio with its date.
- [medium] The title says a GMP site requires validating every change to an installation, but nothing on the slide supports it. The large number (tablet volume) does not prove the title, so the message is split. **Fix:** Add one line with its source, e.g. 'EU GMP, Annexe 15 : toute modification passe par la maîtrise des changements (change control)'. Shrink the 3-milliards block to supporting context.

### Slide 4: Filtres à faible perte de charge (7.3)

message 7, evidence 6, honesty 6, legibility 8, consistency 9, timing 8

- [medium] The chart sets the candidate's replacement threshold at 3 × its own (lower) initial Δp, so 'seuil candidat' sits at 1.8 instead of 3. If the site changes filters at a fixed final Δp in Pa, the candidate's average is (2·0,6+3)/3 = 1,4, not 1,0, and the drawn gain shrinks by about 60 %. The slide does not say which replacement rule the comparator assumes. **Fix:** State the rule on the slide ('seuil = 3 × Δp0, EN 13053, cf. Eurovent 4/24 éq. 3a'). Or draw the candidate with the site's real final Δp and note that the gain depends on this choice.
- [low] The result gives no value (no minimum lifetime, no price ratio), so the slide shows the method but not the answer. **Fix:** Add one result line, e.g. 'rentable si durée de vie ≥ N mois (vs M mois actuels)', or a normalised ratio if the prices are confidential.
- [low] The 'seuil candidat' label sits on the y=2 grid line, above its dashed line at 1.8, and could be read as a threshold at 2. **Fix:** Move the label just above the orange dashed line, or stop the grid line short of the label.

### Slide 7: Trois livrables, trois décisions pour le site (7.8)

message 7, evidence 6, honesty 7, legibility 9, consistency 9, timing 9

- [low] The title says 'trois décisions', but two items are proposals ('Essai pilote proposé', 'Étude de la régulation à engager'); only the rotameter purchase has happened. **Fix:** Retitle 'Trois livrables et leurs suites', or mark each card 'décidé' or 'proposé'.
- [low] The lower third of the slide is empty. **Fix:** Add one line per card with the key figure or owner, or move the cards down to centre them.

### Slide 11: Mode éco : énergie annuelle pondérée par le temps de pesée (8.0)

message 8, evidence 6, honesty 8, legibility 8, consistency 9, timing 9

- [low] The slide carries a data-cite to the 2021 audit (internal, not checkable), but nothing visible on it draws on the audit. The cite looks misplaced; the audit is used for the specific energy on slide 5. **Fix:** Remove the audit2021 cite from R2, or add the quantity it provides (e.g. the source of P_max).
- [low] The heat recovery by the glycol loop (slide 3) does not appear in the energy model, so it is unclear whether E counts gross or net coil energy. **Fix:** Add to the legend: 'énergie des batteries après récupération (boucle glycolée)', or state that the recovery is ignored.

### Slide 1: Évaluation d'économies d'énergie sur un site pharmaceutique sous contrainte GMP (8.2)

message 8, evidence 8, honesty 8, legibility 9, consistency 7, timing 9

- [low] The kicker says 'STAGE M1' but the info block says 'Formation M2 GDP, UGA', and the notes say 'je suis en M2'. A jury may ask which year the internship counts for. **Fix:** Write 'Stage de M1 (2025-2026)' or 'Stage M1 · aujourd'hui en M2 GDP' so both facts are explicit.
- [low] The photo licence rests on 'confirmé par l'auteur du deck auprès d'Adamed', with no written record cited. **Fix:** Keep the e-mail or written permission from Adamed/ALSTAL with the deck sources.

### Slide 5: Banc d'étalonnage de la caméra (8.2)

message 8, evidence 8, honesty 7, legibility 9, consistency 9, timing 8

- [medium] The pressure gauge sits upstream of a hose labelled 'à pression constante'. Under flow, the hose loses pressure, so the gauge reading is higher than the nozzle's p0 and the calculated flow is overestimated. T0, needed in the formula, is not measured on the schematic. **Fix:** Measure p0 at the nozzle inlet, or state that the hose pressure drop was checked and is negligible. Add a thermometer (or 'T0 = température ambiante') to the bench.
- [low] '× 8 760 h (réseau sous pression)' assumes the network is pressurised all year. The data-cite points to Ward-Smith and Fluke, which do not support that assumption. **Fix:** Write 'hypothèse : réseau sous pression 24 h/24, 365 j/an' and cite the 2021 audit or the compressor logs.

### Slide 8: Bilan et enseignements (8.2)

message 7, evidence 6, honesty 9, legibility 9, consistency 9, timing 9

- [low] The first lesson puts two sentences side by side (sensors identified late; one to two weeks lost on filters) without saying how they connect. **Fix:** Rewrite as 'Recenser les capteurs existants avant de calculer : des mesures déjà en place sur les filtres m'auraient fait gagner une à deux semaines.'

### Slide 9: Références (8.3)

message 8, evidence 8, honesty 8, legibility 9, consistency 8, timing 9

- [low] Slide R4 cites the gas-constant source (r_air, Wikipedia 'Gas constant'), but it is missing from the list. The Fluke entry has no URL and no access date, and the pracuj.pl entry has no URL. **Fix:** Add 'Wikipédia, Gas constant, consulté en octobre 2026', and give the URLs or access dates for Fluke ii500 and pracuj.pl.

### Slide 13: Banc : débit d'une buse en écoulement critique (8.5)

message 9, evidence 8, honesty 8, legibility 8, consistency 9, timing 9

- [low] The 1,89 choking threshold assumes an ideal nozzle. For short cylindrical nozzles with sharp upstream edges (the subject of the cited Ward-Smith paper), Cd can vary with the pressure ratio and L/D. The Ward-Smith content itself could not be checked (paywalled). **Fix:** Give the nozzle's L/D, the Cd value used and the pressure ratios tested, and keep a local copy of Ward-Smith 1979 in sources/.
- [low] M_air is written 0,02897 kg/mol; the cited source gives 28,9649 g/mol (0,02896). It makes no difference to R = 287. **Fix:** Write 0,02896 kg/mol or '≈ 0,029 kg/mol'.

### Slide 12: Filtres : perte de charge moyenne selon Eurovent 4/24 (8.8)

message 9, evidence 9, honesty 9, legibility 8, consistency 9, timing 9

- [low] The formula Δp̄ = (2Δp0 + Δpfinal)/3 is Eurovent's condition-based method (filters changed at a predefined final Δp), but the slide does not name that qualifier. **Fix:** Add '(méthode « condition based » : remplacement au seuil Δp_final, éq. 3)' to the legend.

## Not verified (source unreachable)

- Slide 2: plus de 3 milliards de comprimés par an (groupe Adamed) (adamed_pracuj)
- Slide 5: énergie spécifique de l'audit 2021 (audit2021)
- Slide 11: R2 cite l'audit énergétique 2021 (audit2021)
- Slide 13: C_d : coefficient de décharge (Ward-Smith 1979) (ward_smith_1979)
