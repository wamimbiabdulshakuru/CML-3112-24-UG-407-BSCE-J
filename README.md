# Course Code: CML3112
## Program: BSCE-J (Civil Engineering)
### Cohort: CML3112

### 1. Project Description
This engineering repository processes structural health data from an automated survey tracking concrete slab degradation. The program evaluates concrete slab crack propagation logs over a dataset of 300 inspection entries to clean missing values, isolate severe threshold exceptions, and calculate localized structural metrics.

### 2. Files List
* `24_UG_407_BSCE_J_W04.ipynb` - The completed Week 4 data processing assignment notebook containing evaluation code configurations, structural calculations, and analytical evidence cells.
* `site_inspection.log` - The source Microsoft Excel Comma-Separated Values format log containing 300 raw inspection rows tracking crack width measurements.
* `README.md` - The repository deployment instructions and student identity declaration document.

### 3. Structural Evaluation Summary & Patterns
* **Data Cleaning Pattern:** Out of 300 total logged entries, exactly 3 entries contain missing data. The script applies clean string filtering (`!= ''`) to isolate 297 valid records, calculating an absolute unrounded mean reading of `0.2262996632996631 mm`.
* **Safety Threshold Pattern:** By implementing a strict greater-than nested condition (`> 0.3`), the code filters out standard surface wear to isolate exactly 59 critical structural cracks that violate safe operating parameters.
* **Localized Clustering Pattern:** Utilizing dynamic dictionary key grouping across unique location tags (`B1` through `B9`) reveals that crack development is localized rather than uniform. This indicates targeted sub-surface settlement variations or localized stress distributions across specific structural blocks.

### 4. How to Run
1. Launch **Google Colab** in your web browser.
2. Select the **Upload** tab, click browse, and upload your notebook file: `24_UG_407_BSCE_J_W04.ipynb`.
3. Open the left vertical sidebar panel by clicking the **Folder icon** (Files).
4. Click the **Upload to session storage** icon and select the source dataset file: `site_inspection.log`.
5. Open the **Runtime** menu option from the top navigation bar and select **Restart and run all** to process all code blocks sequentially from top to bottom.
