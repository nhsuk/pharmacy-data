# Pharmacy data

This repo is used to maintain a record of how pharmacy data retrieved from the
NHS Choices Organisation API changes over time.

Whenever a new `pharmacy-list.json` file is available it is pretty printed
(so that readable diffs can be generated) with:
```
cat pharmacy-list.json | python -m json.tool > pharmacy-list.json
```

Once the file is formatted, a report is generated with:
```
  git diff <current-hash> <previous-hash> --unified=0 --word-diff=plain > report-name.txt
```
and saved in `/diffs`.

The report is named using the format
`data-diff-<previous-date>-<current-date>.txt` e.g. a report run comparing
a data set from 01/10/2016 to 10/10/2016 would have the name
`data-diff-20161001-20161010.txt`.

In order for the diff report to contain only the changes in `pharmacy-list.json`
the file should be comitted on its own.

