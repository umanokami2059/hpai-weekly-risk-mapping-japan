# Known issues and disclosure items before public release

## 1. Original rolling-training notebook not located — TRANSPARENTLY DISCLOSE
- Recorded notebook version: `06_v2_rolling_riskmap_evaluation_previous_week_weather_final`.
- The original source notebook was not located during the audit.
- Archived outputs, 12 fitted Random Forest model files, 12 prediction parquet files, feature definitions, split checks, and validation summaries remain available.
- A documented replacement implementation is included in `06_v2_FAST_VERIFY_and_OPTIONAL_RETRAIN.ipynb`.
- On 19 September 2026 the fast validation reproduced the manuscript Table 2 values exactly from the archived predictions.
- Do not describe the replacement notebook as the original historical source file. Describe it as a documented reconstruction/verification implementation.

## 2. Software-version discrepancy — FIX IN SECOND REVISION
- Executed `14_v7` output: Python 3.12.13, pandas 2.2.2.
- First-revision manuscript statement: pandas 2.2.3.
- Action: harmonize the manuscript and public repository with the execution record unless contrary evidence is found.

## 3. Historical land-use source cap — DISCLOSE, DO NOT SILENTLY REPLACE
- Historical `18_v8` code: `MAX_FILES_TO_PROCESS = 120`.
- Later audit: 135 candidate unique tiles; 60 unique tiles processed before the cap; 75 omitted.
- Historical processed-feature availability: 4,095/5,491 grids.
- Later full-unique-tile availability: 4,512/5,491 grids.
- Preserve manuscript wording that these are missing values in the processed feature set used for the reported analysis.

## 4. Later reanalyses are not the source of the submitted numerical results — EXCLUDE FROM PRIMARY REPO
Do not present `FINAL_MASTER_REANALYSIS_V2`, `14_v9_*`, later full-tile GIS reanalyses, or training-identity experiments as the analysis that produced the submitted manuscript values. They are internal diagnostic/reanalysis artifacts.

## 5. Large archived files
The exact rolling verification depends on the archived prediction parquet files. For the permanent public release, place large prediction/model artifacts in a versioned archive such as Zenodo and cite the DOI. Do not rely on private Google Drive paths in the final public documentation.
