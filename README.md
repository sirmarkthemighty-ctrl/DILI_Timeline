# LiverTox DILI Timeline
### Drug-induced liver injury: exposure windows against liver chemistry, read against NIDDK LiverTox

A bedside and teaching tool for working up suspected drug-induced liver injury (DILI), by
Warodom Phaenthong, M.D. It is one self-contained HTML page (`dili-timeline.html`, opened by `index.html`)
that runs in the browser, with no installation and no data sent anywhere — the case you type stays in your
own browser's local storage.

It is decision support for healthcare professionals. It does not establish causality and does not replace
the LiverTox record, your hospital's protocols, clinical judgement or formal RUCAM adjudication.

**Open it:** https://sirmarkthemighty-ctrl.github.io/DILI_Timeline/

## What it does

- **One shared time axis.** Drug exposure bars and every liver test are drawn on the same scale, so latency
  and dechallenge line up vertically. Long stretches with no drug event and no blood draw collapse to a
  marked break (switchable back to a strictly proportional axis), so a drug started years before the injury
  does not squash the period that matters.
- **Onset marker.** A dashed line at the first draw meeting the biochemical threshold for DILI
  (ALT ≥5× ULN, or ALP ≥2× ULN, or ALT ≥3× with bilirubin ≥2×), which is what makes latency readable.
- **Per agent:** latency, a CIOMS/RUCAM timing verdict (5–90 days compatible; onset ≤15 days after stopping
  still counts), dechallenge (≥50% fall in the leading analyte after the drug stopped), and whether the
  patient's injury pattern matches the agent's typical one.
- **R value computed at onset**, not only on the latest draw, with the hepatocellular / mixed / cholestatic
  zones drawn as its own panel. Hy's Law and coagulopathy-with-jaundice are flagged.
- **Editable upper limits of normal** — every R value, threshold and Hy's Law check recalculates from your
  own laboratory's limits.
- **310 LiverTox agents** with likelihood category (A–E) and typical injury pattern, searchable by generic
  name, brand name, drug class or pattern.
- **A4 report export** — page one the timeline and both data tables, page two the assessment and references —
  as a real PDF or two JPGs; plus CSV of the raw case data.
- Colour-coded folding sections, light and dark themes, phone layout.

Tap the version badge next to the title for the changelog.

## Citations and what is missing

Likelihood categories and injury patterns are **condensed from LiverTox, not quoted**. Of the 310 agents,
**9 link to a verified NCBI Bookshelf chapter id**; the rest resolve through LiverTox search and are marked
**N/A · search** rather than being dressed up as a citation. The References panel states this coverage for
the case on screen and for the whole set. Open the linked chapter for the authoritative entry.

Core references used by the calculations:

- LiverTox, NIDDK — https://www.ncbi.nlm.nih.gov/books/NBK547852/
- Danan G, Benichou C. J Clin Epidemiol. 1993;46(11):1323–30 (CIOMS/RUCAM timing)
- Aithal GP, et al. Clin Pharmacol Ther. 2011;89(6):806–15 (case definition, R value)
- Hoofnagle JH, Björnsson ES. N Engl J Med. 2019;381(3):264–73
- FDA, Drug-Induced Liver Injury: Premarketing Clinical Evaluation, 2009 (Hy's Law)

## Editing

The page is currently hand-edited as a single file; there is no build step. Open `dili-timeline.html`
in a browser to check a change, and check the phone layout at 375 px before publishing.

## Licence

Code, layout and calculators: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International
(CC BY-NC-SA 4.0) — see `LICENSE` and `NOTICE`. The LiverTox content summarised in the agent list belongs
to its authors at the NIDDK.
