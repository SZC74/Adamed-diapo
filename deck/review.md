# Deck review: 7.8 / 10

Reviewer: subagent
Build: `5cae9de6717705a6` · 2026-10-21T17:47:10

Clear, honest storyline (three energy topics under GMP constraint, each ending in a decision) and every formula I could check is correct: Eurovent 4/24 Eq. (1) and (3), the EN 13053 x=3 threshold, the choked-flow equation (Psi = 0.685, critical ratio 1.893, R = 287) and the CDC isolation-room principle all hold. The weakest point is evidence: the main slides carry no quantified result at all (gains internal, values masked), the 8 760 h and L/min figures hide unstated assumptions (continuous pressurisation, reference conditions), and two cited sources (pracuj.pl for the 3 billion tablets, the 2021 audit) could not be opened.

| Gate | Count |
|---|---|
| failed source checks | 0 |
| unsourced numbers | 0 |
| images without credit/licence | 0 |
| image problems | 1 |

## Images

- **Slide 1**: Aerial photo of the Adamed production and logistics centre in Pabianice (ADAMED logos visible; ALSTAL was the contractor for this centre, consistent with the credit). The credit is shown, but the licence is recorded as 'autorisation d'usage non documentée'. Documented permission is needed before the deck is sent or posted.

## Slides, lowest score first

### Slide 3: Mode éco des cabines de pesée : réduction du débit d'air neuf hors pesée (7.2)

message 7, evidence 4, honesty 7, legibility 8, consistency 9, timing 8

- [medium] The conclusion 'gain brut ... suffisant pour justifier une étude' rests on no visible number: no order of magnitude, share or input value is shown, so the jury has to take the result on trust. **Fix:** If the amounts are confidential, show a relative value (for example 'about X % of the booths' HVAC energy' or a rounded MWh/an range), or at least the drivers (τ, flow reduction ratio, 1 year of supervision data).
- [low] The method (one year of supervision data, millions of rows, Python recalculation at reduced flow) appears only in the speaker notes. **Fix:** Add one line under the diagram: 'Méthode : 1 an de supervision, recalcul à débit réduit (détail R2)'.

### Slide 6: Application de traitement des relevés : débit et coût annuel par fuite (7.2)

message 7, evidence 5, honesty 6, legibility 8, consistency 8, timing 9

- [medium] Flow is shown in L/min with no reference conditions. The nozzle gives a mass flow, and the audit's specific energy refers to a defined volume (free air or normal m³), so the cost depends on that choice. **Fix:** Label the unit 'NL/min (1,013 bar, 0 °C)' or 'L/min d'air libre', matching the basis of the audit's kWh/m³.
- [medium] 'débits réels inférieurs au domaine du banc' gives no numbers, so the size of the extrapolation problem is invisible. **Fix:** Give both ranges, for example 'banc : x–y NL/min ; fuites relevées : typiquement < z NL/min'.

### Slide 11: Mode éco : énergie annuelle pondérée par le temps de pesée (7.3)

message 7, evidence 5, honesty 7, legibility 8, consistency 8, timing 9

- [medium] E_réduit, the term the whole gain depends on, is not defined: the slide does not say how the reduced flow changes the coil and fan energy (same enthalpy change per m³? fan affinity law?). **Fix:** Add one line, for example 'E_réduit : mêmes Δh par m³ d'air × débit réduit ; ventilateur : P ∝ q³ (ou mesure)'.
- [low] The 2021 audit is attached to this slide but nothing on it uses the audit, and E has no unit. **Fix:** Move the audit2021 cite to slide 5 and add 'E : kWh/an'.

### Slide 4: Filtres à faible perte de charge : perte de charge moyenne selon Eurovent 4/24 (7.5)

message 7, evidence 7, honesty 7, legibility 8, consistency 8, timing 8

- [medium] The illustrative profiles give the candidate filter a lifetime about 1.3 times the current one, while the 'Coût' box says its lifetime is unknown and must be found by a pilot test. The figure presents as given what the slide says is open. **Fix:** Draw both filters with the same lifetime (the energy comparison does not depend on it under the condition-based method), or label the candidate cycle 'durée de vie supposée, à mesurer'.
- [low] The orange 'moyenne, candidat' dotted line sits exactly on the current filter's clean level (1.0), where the teal curve restarts, so the two read as one line. **Fix:** Add a tick label 'Δp0 actuel' at 1 and make the candidate mean line heavier, or move its label next to the line end.
- [low] The title names the method, not the finding. **Fix:** For example: 'Filtres : gain d'énergie calculable (Eurovent 4/24), rentabilité suspendue à la durée de vie'.

### Slide 5: Banc de référence : buse calibrée en écoulement critique (7.5)

message 8, evidence 7, honesty 6, legibility 8, consistency 8, timing 8

- [medium] 'débit × 8 760 h' assumes the compressed-air network is pressurised all year, and the slide does not say so. If the network is shut down at weekends or during stoppages, the leak cost is overstated. **Fix:** Write '8 760 h (réseau sous pression en continu, hypothèse)' or use the network's actual pressurised hours from the 2021 audit.
- [medium] No source is visible on the slide. In the data, 8 760 h is cited to Ward-Smith 1979 and the Fluke ii500, which do not contain it, and the 'énergie spécifique (audit 2021)' is not linked to the audit source (that link sits on slide 11). **Fix:** Add a source line 'Ward-Smith 1979 ; Wikipédia, Choked flow ; Fluke ii500 ; audit énergétique 2021', move the audit2021 cite here, and mark 8 760 h as a calculation (365 × 24).
- [low] The bench's pressure and flow range is not given, so slide 6's statement that field flows fall below the bench domain cannot be judged. **Fix:** Add the tested range, for example 'p0 = a–b bar, débit = x–y NL/min', in the calibration box.

### Slide 1: Évaluation d'économies d'énergie sur un site pharmaceutique sous contrainte GMP (7.8)

message 8, evidence 7, honesty 7, legibility 9, consistency 7, timing 9

- [medium] The aerial photo is credited, but its licence is recorded as 'autorisation d'usage non documentée' (Adamed press photo by ALSTAL). **Fix:** Get a written OK from Adamed communications (an e-mail is enough) and record it in sources.json, or replace it with a photo you took or one with a stated licence.
- [low] The kicker says 'STAGE M1' but the Formation field says 'M2 GDP', and the notes open with 'je suis en M2'. A jury may read this as a contradiction. **Fix:** Write 'Stage de M1 · présenté en M2' or 'Formation : M2 GDP (stage réalisé en M1)'.

### Slide 2: Site pharmaceutique sous GMP : toute modification d'installation est soumise à validation (7.8)

message 7, evidence 6, honesty 7, legibility 9, consistency 9, timing 9

- [medium] The cited source for '3 milliards de comprimés par an' (pracodawcy.pracuj.pl) returns HTTP 403 and cannot be checked. Trade press found by search gives about 3.2 billion tablets a year, which is consistent but is not the cited page. **Fix:** Cite a reachable, dated source (Adamed press release or annual report, or an archived copy of the pracuj page) and keep 'groupe Adamed' as the qualifier.
- [low] The title claims that any change to an installation must be validated under GMP. That is the key constraint of the talk, but nothing on the slide supports it, while the big number (group output) does not support the title. **Fix:** Add a short source line such as 'EU GMP, Annexe 15 (qualification et validation, maîtrise des changements)', or shrink the 3 milliards block so the GMP constraint becomes the visual focus.

### Slide 8: Bilan et enseignements (7.8)

message 7, evidence 6, honesty 8, legibility 9, consistency 9, timing 8

- [low] The generic title 'Bilan et enseignements' wastes the last impression. **Fix:** Lead with the main lesson, for example 'Bilan : voir l'installation avant de calculer'.

### Slide 9: Références (8.0)

message 8, evidence 8, honesty 8, legibility 8, consistency 7, timing 9

- [low] R = 287 J/(kg·K) on R4 is cited to Wikipedia 'Gas constant', which is missing from the list. The Fluke and Wikipedia entries have no URL, and the Fluke entry has no access date. **Fix:** Add 'Wikipédia, Gas constant, consulté en octobre 2026' and the URLs with access dates for the web entries.

### Slide 13: Banc : débit d'une buse en écoulement critique (8.0)

message 8, evidence 8, honesty 8, legibility 7, consistency 8, timing 9

- [low] Cd is attributed to Ward-Smith 1979, but the value used, and the nozzle L/D it depends on, are not given. **Fix:** Add 'Cd = … (L/D = …, Ward-Smith 1979)'.
- [low] 'au-dessus de 1,2^3,5 = 1,89' is easy to misread with decimal commas in the exponent, and the four-line legend is dense. **Fix:** Write 'valable si p0/patm > 1,89 (= 1,2^3,5 pour γ = 1,4)' and split the legend into two short lines.
- [low] The molar mass of air is given as 0,02897 kg/mol. The cited source gives 28.964917 g/mol, i.e. 0,02896 kg/mol (no effect on 287). **Fix:** Write 0,02896 kg/mol.

### Slide 7: Livrables et décisions associées (8.2)

message 8, evidence 6, honesty 8, legibility 9, consistency 9, timing 9

- [low] The title is a topic label. The slide's point (each deliverable hands a decision to the site) is only in the subheading. **Fix:** Use a message title, for example 'Trois livrables, trois décisions désormais entre les mains du site'.

### Slide 12: Filtres : perte de charge moyenne selon Eurovent 4/24 (8.2)

message 8, evidence 9, honesty 8, legibility 8, consistency 7, timing 9

- [low] Eq. (3) applies only to the condition-based method (filter changed at Δpfinal), and the slide does not say so. W has no unit. **Fix:** Add 'méthode à seuil (condition based), Eurovent 4/24 Éq. (1) et (3) · W : kWh/an', and state the t and η used (Eurovent defaults: 6 000 h/a, η = 0,5).
- [low] The legend sets Δp0 and Δp_final in italic with an italic subscript, while the equation uses an upright Δ and a roman 'final'. **Fix:** Typeset the legend symbols the same way as the equation.

### Slide 10: Cascade de pression : l'air s'écoule de la pression la plus haute vers la plus basse (8.5)

message 9, evidence 8, honesty 8, legibility 9, consistency 8, timing 9

- [low] The diagram is correct against CDC 2003, but no source is shown on the slide. **Fix:** Add 'Source : CDC, MMWR 52 (RR-10), 2003' under the diagram.

## Not verified (source unreachable)

- Slide 2: Groupe Adamed : plus de 3 milliards de comprimés produits par an (adamed_pracuj)
- Slide 5: énergie spécifique (audit 2021) (audit2021)
- Slide 11: Mode éco : énergie annuelle pondérée par le temps de pesée (audit 2021 cité) (audit2021)
- Slide 13: Cd : coefficient de décharge (Ward-Smith 1979) (ward_smith_1979)
