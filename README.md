# Pharmacy data

This repo is used to maintain a record of how pharmacy data retrieved from the NHS Choices Organisation API changes over time.

Each time `pharmacy-data.json` is updated a report is generated with the
following command and saved in `/diffs`.

```
  git diff <current-hash> <previous-hash> --unified=0 --word-diff=plain
```
