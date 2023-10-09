# steel_construction_manual_tables

# Run it locally

This script parses steel_construction_manual_tables into code-readable csv format
(add link to book here + edition details)

## Prerequisites

- Python 3.x installed on your machine.
- Necessary Python packages installed. Install the required packages using the following command:

  ```bash
  pip install pandas  

- Upload the pdf file and db file under input_files
- Edit code to handle names of files
- Run code

# `2023.10.03` Integrity Check

Compare ` w_shapes`` table to  `Wshapes_Table6_1`

- `w_shapes` is generated from an opensource library
- `Wshapes_Table6_1` is generated from AISC 15th Edition

### Comparison:

1. Look at each item in `w_shapes`
2. find it's counterpart in `Wshapes_Table6_1`
   - search by `profile`, `length_ft`, `Cb`, and `Pr_over_Pc`
3. If it can find a match, run the comparison
4. if results are within 5%, consider it passing, otherwise store it as a failure
   - check `Pr_k`, `Pc_k`, `Mmax_ftk`, `Mc_ftk`
5. Would like a report that shows:
   - How many passed
   - How many failed
   - List of items that failed

```
percentDiff = (|x1 - x2| / ((x1 + x2)/2)) * 100
```
