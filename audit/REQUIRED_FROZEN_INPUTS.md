# Frozen inputs required to reproduce the reported analysis

The following files should be checksummed and either archived with the release (subject to redistribution terms) or documented with an exact derivation/download procedure:

1. `hpai_weekly_grid_panel_with_previous_week_weather_model_ready.parquet`
   - archived Drive size: 19,440,957 bytes
   - reported rows: 1,641,809
   - grids: 5,491
2. `18_v8_grid_environment_features_for_14.parquet`
   - archived Drive size: 524,903 bytes
   - exact historical GIS/land-use feature matrix used by `14_v7`
3. `10_event_occurrence_type_classification.csv`
   - event classification used to fix the 49 strict first-occurrence-like events in the primary analysis
4. Archived `06_v2` prediction/model outputs for the 3 fiscal-year splits × 4 predictor sets.
5. `14_v7_all_grid_predictions_event_weeks.parquet`
   - archived Drive size: 5,212,619 bytes
   - exact saved strict-event weekly predictions used by the sensitivity analysis and later figure generation.

Do not substitute the later full-unique-tile GIS matrix for item 2 without rerunning and revising the manuscript.
