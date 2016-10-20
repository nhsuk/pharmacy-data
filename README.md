# Pharmacy data

This repo is used to maintain a record of how pharmacy data retrieved from the
NHS Choices Organisation API changes over time.

Each time `pharmacy-data.json` is updated a report is generated with the
following command and saved in `/diffs`. The report is named using the format
of `data-diff-<previous-date>-<current-date>.txt` e.g. a report run comparing
a data set from 01/10/2016 to 10/10/2016 would have the name
`data-diff-20161001-20161010.txt`

```
  git diff <current-hash> <previous-hash> --unified=0 --word-diff=plain
```
