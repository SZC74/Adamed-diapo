# Deck review: 7.5 / 10

Reviewer: subagent
Build: `d768d0032c4616c6` · 2026-10-21T16:10:33

The deck is clean and honest about the limits of each study. The diagrams for the eco mode, the critical-flow bench and the Eurovent filter profiles explain the method clearly, and the backup equations (Eurovent Eq. 1 and 3, the choked-nozzle law with Psi = 0.685 and the 1.89 ratio) check out against their sources. Its weakest point is that an energy-savings deck never shows a single quantified saving: slides 3, 6 and 7 assert that gains justify further work but show no kWh, PLN or %, and the filters slide's notes present an estimate as certain ("le gain d'énergie est sûr"), although Eurovent calls its method a rough estimate that also needs a variable-speed fan. Backup slide R2 cites a source key (audit2021) that matches no reference.

| Gate | Count |
|---|---|
| failed source checks | 2 |
| unsourced numbers | 0 |
| images without credit/licence | 0 |
| image problems | 0 |

## Source checks that failed

- **Slide 4: Notes : « Le gain d'énergie est sûr »**: qualifier mismatch (eurovent_424). Source: “can be used as a rough estimation ... requires that the speed of the fan can be adjusted to supply a constant air volume flow rate”. The source presents the result as an estimate that depends on a variable-speed fan. The talk presents it as certain.
- **Slide 11: Modèle E_an = τ E_plein + (1−τ) E_réduit ; P_batterie = u P_max (cité audit2021)**: not found (audit2021). sources.json: « aucune référence correspondante dans la liste du deck (source à identifier) ». There is no citation, URL or file. The cited source does not exist.

## Slides, lowest score first

### Slide 11: Mode éco : énergie annuelle pondérée par le temps de pesée (6.3)

message 7, evidence 3, honesty 3, legibility 9, consistency 8, timing 8

- [high] The slide cites 'audit2021', which sources.json describes as 'aucune référence correspondante dans la liste du deck (source à identifier)'. The eco-mode model is credited to a source that does not exist in the deck. **Fix:** Either cite the actual site audit (title, author, date) and add it to slide 9, or remove the citation and label the model 'modèle de l'auteur, hypothèses ci-dessous'.
- [medium] Only the heating and cooling coils are modelled (P = u·Pmax). The fan electricity saved at reduced flow is not mentioned, and the slide does not say how τ was measured. **Fix:** Add a line: 'ventilateur : [inclus via loi de similitude / négligé]' and 'τ mesuré sur [registre de pesée / signal de présence], valeur Z %'.

### Slide 4: Filtres à faible perte de charge : perte de charge moyenne selon Eurovent 4/24 (6.5)

message 7, evidence 6, honesty 3, legibility 7, consistency 8, timing 8

- [high] The notes say 'Le gain d'énergie est sûr'. Eurovent 4/24 calls its result 'a rough estimation' and says the saving 'requires that the speed of the fan can be adjusted to supply a constant air volume flow rate'. With a fixed-speed fan the flow rate rises instead, and consumption can even go up. **Fix:** Say 'gain estimé selon la convention Eurovent, à condition que le ventilateur soit à vitesse variable (débit constant)' and add this condition to the Énergie box. State whether the site's AHU fans are variable-speed.
- [low] The chart gives the candidate filter a lower replacement threshold (≈1.8) than the current one (3). The gain shown depends on that illustrative choice, and the slide does not say whether the site would keep the same threshold. **Fix:** Draw both filters with the site's real threshold rule (same Δp_final, or the manufacturer's value), or add 'seuils illustratifs' next to the threshold labels.
- [low] The candidate's mean line (y = 1) sits at the same level as the current filter's clean value, and the end of the teal curve is hidden under the orange one near x = 2.6. The 'écart : gain' gap is therefore hard to read. **Fix:** Add a bracket or arrow between the two dotted mean lines labelled 'gain', and end both curves at the same x before they overlap.

### Slide 3: Mode éco des cabines de pesée : réduction du débit d'air neuf hors pesée (6.7)

message 7, evidence 3, honesty 6, legibility 8, consistency 9, timing 7

- [high] The conclusion says 'le gain brut justifie une étude', but the slide gives no gain at all: no kWh/an, no PLN/an, no % of AHU energy, no value of tau. The jury cannot judge whether the gain justifies anything. **Fix:** Add one number with its basis next to the diagram, e.g. 'gain brut estimé : X MWh/an (Y PLN/an), τ = Z %, 1 an de supervision'. If the values are confidential, say so and give an order of magnitude or a % of the cabin's energy.
- [low] The notes rely on 'un an de données, plusieurs millions de lignes', but neither the period nor the data source appears on the slide. **Fix:** Add a source line: 'Données : supervision GTC, [mois année]–[mois année], pas de N min'.

### Slide 6: Application de traitement des relevés : débit et coût annuel par fuite (7.0)

message 7, evidence 3, honesty 7, legibility 8, consistency 9, timing 8

- [high] The values are masked on the mockup, and the claim that field results were 'assez cohérents pour justifier l'achat d'un rotamètre' (notes) is not quantified. The leak study shows no result and no calibration curve. **Fix:** Show the bench calibration (flow vs score and vs dB, with the calibrated range shaded) or at least 'N fuites relevées, écart score/dB ±X %'. If the values are confidential, write 'valeurs confidentielles' rather than just 'masquées'.
- [low] 'Photo de la caméra : score, dB et distance' is fine for the ii500 (Fluke: 'Leak size scale (1-10)', 'distance-estimation feature'). Fluke's higher models (ii905/ii915) do give leak rate and cost, so the jury may ask why they were not used. **Fix:** Prepare a one-line answer, e.g. 'ii500 disponible sur site ; les ii905/915 estiment le débit mais sans référence locale'.

### Slide 9: Références (7.3)

message 8, evidence 6, honesty 6, legibility 9, consistency 6, timing 9

- [medium] The list does not match the sources used: the Wikipedia 'Gas constant' page (r_air, cited on R4) is missing, and R2 cites a key 'audit2021' that matches no reference. **Fix:** Add 'Wikipédia, Gas constant, consulté en octobre 2026'. Either add the real audit reference used for the eco-mode model, or remove the audit2021 citation from R2.
- [low] The Ward-Smith and Fluke entries are incomplete: Ward-Smith has no volume, pages or DOI, and Fluke has no URL, date or manual version. **Fix:** Complete them: Ward-Smith with volume(issue), pages and DOI; Fluke with the URL and the manual edition and date.

### Slide 5: Banc de référence : buse calibrée en écoulement critique (7.5)

message 8, evidence 5, honesty 7, legibility 9, consistency 8, timing 8

- [medium] The critical-flow formula (R4) needs the upstream temperature T0, but the bench shows only a pressure gauge. Neither the nozzle size nor the pressure and flow range of the bench is given. **Fix:** Add a thermometer, or the note 'T0 = température ambiante', to the diagram, plus one line with the bench domain: 'buse Ø x mm, p0 = a–b bar, débit = c–d L/min'.
- [low] The slide cites Fluke and Ward-Smith 1979 in its markup, but no source is visible. The Ward-Smith paper has no URL or local copy, so it could not be checked. **Fix:** Add a small source line 'Réf. 2, 3', and give the Ward-Smith entry its volume, pages and DOI in sources.json and on slide 9.

### Slide 2: Site pharmaceutique sous GMP : toute modification d'installation est soumise à validation (7.7)

message 6, evidence 6, honesty 8, legibility 9, consistency 9, timing 8

- [medium] The title claims that every change to an installation must be validated under GMP. Nothing on the slide supports it: the biggest element is the group's tablet count, which says nothing about the constraint. **Fix:** Add a one-line reference for the change-control requirement (EU GMP Annex 15, qualification and validation / change control) under the DÉMARCHE band, or move the GMP sentence into the DÉMARCHE band and make the title about the three topics.
- [low] The '3 milliards' figure is a group-wide number taken from an undated employer profile. More recent press figures (PAP) give about 3.5 billion per year, so 'plus de 3 milliards' is still true. **Fix:** Keep 'plus de 3 milliards', and write 'groupe Adamed, tous sites' in the label so nobody reads it as Pabianice output.

### Slide 7: Livrables et décisions associées (7.7)

message 8, evidence 4, honesty 7, legibility 9, consistency 9, timing 9

- [medium] The summary lists deliverables and decisions but no outcome size. None of the three cards carries the estimated saving that would make each decision worthwhile. **Fix:** Add one figure per card under the title (e.g. '≈ X MWh/an', 'Δp moyen −Y %', 'Z PLN/an par fuite type'), or 'non chiffré' where nothing could be quantified.

### Slide 1: Évaluation d'économies d'énergie sur un site pharmaceutique sous contrainte GMP (7.8)

message 8, evidence 7, honesty 7, legibility 9, consistency 7, timing 9

- [medium] The source entry for the aerial photo records its licence as 'autorisation d'usage non documentée'. The photo comes from a construction firm's press office (ALSTAL) via Adamed. Adamed's news page about ALSTAL's Pabianice extension shows no such credit. **Fix:** Get written permission from Adamed communications (or use an Adamed image whose use is documented) and record it in sources.json before the deck PDF is circulated.
- [low] The kicker says 'STAGE M1' and the Formation cell says 'M2 GDP, UGA'. Read side by side, the jury may take them as a contradiction. **Fix:** Make it explicit, e.g. kicker 'STAGE DE M1 / ADAMED PHARMA' and Formation 'M2 GDP, UGA (en cours)'.

### Slide 10: Cascade de pression : l'air s'écoule de la pression la plus haute vers la plus basse (7.8)

message 8, evidence 6, honesty 8, legibility 9, consistency 8, timing 8

- [low] The cascade is explained with a hospital analogy and no source. A pharma jury may ask for the GMP equivalent (typical Δp between grades). **Fix:** Add one line with a pharmaceutical reference, e.g. 'GMP : 10–15 Pa entre classes adjacentes (EU GMP Annexe 1)', or the site's actual setpoint for the weighing booth.

### Slide 8: Bilan et enseignements (8.0)

message 8, evidence 6, honesty 8, legibility 9, consistency 9, timing 8

- [low] The competences are generic ('Traitement de données volumineuses') and are not tied to the evidence on earlier slides. **Fix:** Make them concrete with the scale: e.g. 'Python : 1 an de supervision, ~N millions de lignes'.

### Slide 13: Banc : débit d'une buse en écoulement critique (8.2)

message 8, evidence 8, honesty 8, legibility 8, consistency 9, timing 8

- [low] The Cd value used is not given and its source (Ward-Smith 1979) could not be checked: there is no URL or copy. The legend wraps onto a second line in small type. **Fix:** Give the Cd value used (e.g. 'Cd ≈ 0,8x pour L/D = …') with its page in Ward-Smith, and split the legend into two shorter lines.

### Slide 12: Filtres : perte de charge moyenne selon Eurovent 4/24 (8.5)

message 8, evidence 9, honesty 8, legibility 9, consistency 9, timing 8

- [low] The legend gives units for every input but not for the result W. Eurovent gives W in kWh/year. The slide also omits the source's condition that the fan must keep a constant flow (variable speed). **Fix:** Append 'W : énergie annuelle (kWh)' to the legend and 'valable à débit constant (ventilateur à vitesse variable)'.

## Not verified (source unreachable)

- Slide 5: Au-delà du rapport de pression critique, débit indépendant de l'aval (buse, Ward-Smith 1979) (ward_smith_1979)
- Slide 13: Cd : coefficient de décharge (Ward-Smith 1979) (ward_smith_1979)
