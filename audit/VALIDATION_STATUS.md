# Validation status — 19 September 2026

## Rolling fiscal-year evaluation

The fast validation notebook `code/03_rolling_evaluation/06_v2_FAST_VERIFY_and_OPTIONAL_RETRAIN.ipynb` was executed against the archived `06_v2` prediction parquet files.

Result:

`SUCCESS — ARCHIVED 06_v2 PREDICTIONS REPRODUCE THE MANUSCRIPT TABLE 2 VALUES.`

This establishes that the preserved prediction outputs independently reproduce the rolling event-level metrics reported in manuscript Table 2, including the Top 1%, Top 5%, Top 10%, Top 20%, event-risk-percentile, and rank summaries.

This validation does **not** establish bitwise regeneration of the archived predictions from a newly refitted Random Forest pipeline. The original `06_v2_rolling_riskmap_evaluation_previous_week_weather_final` source notebook was not located. A documented full-refit implementation is included as an optional section in the verification notebook, but is disabled by default because it is computationally intensive and exact refitting may depend on the original runtime and training-row provenance.

## Strict event-week evaluation

The executed `14_v7` notebook and archived result tables are preserved. These support the submitted strict-event values and the paired bootstrap / exact-transition results.

## Sensitivity analysis

The `14_v13` sensitivity notebook uses the saved final `14_v7` predictions rather than refitting the strict models. It reproduces the alternative first-occurrence definitions reported in Supplementary Table S5.
