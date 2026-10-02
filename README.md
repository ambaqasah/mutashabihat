# Quran-Similarities: Verbally Similar Verses (al-Mutashābih al-Lafẓī) in the Quran

Data released with the paper *Detecting and Localizing Verbally Similar Verses (Mutashabihat) in the Quran: An Expert-Derived Benchmark and Alignment-Aware Methods for Memorization Support*.

## Data files

`benchmark/`
- `benchmark_verses.csv` — 1,239 annotated rows from *Hidāyat al-Murtāb* and *Tatimmat al-Bayān*, with surah, ayah, Juz, verse text, connection group, change type and notes.
- `benchmark_pairs.csv` — 2,229 positive verse pairs derived from the connection groups.
- `benchmark_verses.xlsx`, `benchmark_pairs.xlsx` — Excel copies of the two files above.

`results/`
- `discovery_candidates_for_expert_review.csv` — the 200 highest-scored verse pairs that are not in the benchmark, for expert review.
- `localization_predictions_L2.csv` — confusable spans predicted by the group anchor + divergence method (L2).
- `revision_card_examples.csv` — example revision cards.
- All other files are the intermediate results behind the tables and figures of the paper (retrieval, re-ranking, localization, change-type prediction, and confusability profiles).

All files are UTF-8 CSV files that use the standard `surah:ayah` key format (e.g., `2:59`); because Microsoft Excel converts such keys to times when a CSV is opened by double-clicking, Excel users should open the provided `.xlsx` copies or import the CSV via *Data → From Text/CSV* with the key columns set to *Text*.

The Quran text is the Tanzil Simple-Clean edition (https://tanzil.net), used under its terms.
