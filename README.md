# steel_construction_manual_tables

Parsed steel_construction_manual_tables into code-readable csv format

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
