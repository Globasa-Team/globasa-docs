# Globasa Docs

A location for technical documents regarding the API backend, data files, and translation dictionary website views.

> [!CAUTION]
> API v1 is deprecated soon. Please upgrade to API v2 ASAP. The files will be removed from the `api.globasa.net` website, and are temporarily copied to `cdn.globasa.net/api1`.

> [!NOTE]
> Globasa Team projects use 3-letter language codes when referencing natlang languages.

## Parsed files that will remain consistent
* [Standard translation data endpoint](api2-standard.md)

## Parsed files that may change
* https://cdn.globasa.net/api2/index.json / .yaml - All Globasa terms, including alternate forms
* search_terms_[???].json / .yaml - parsed natlang search terms from translations. 
* min_[???].json / .yaml - parsed natlang key/value for globasa term => natlang translations string.

## Files that will be wildly inconsistent
https://cdn.globasa.net/api2/

Any files not otherwise listed may change wildly as the translation dictionary website's sepcifications change.

## Unprocessed files:
  * https://cdn.globasa.net/api2/word-list.csv
  * https://cdn.globasa.net/api2/word-list.ods
  * https://cdn.globasa.net/api2/word-list.tsv
  * https://cdn.globasa.net/api2/word-list.xlsx

## Participate

Join the [Globasa Discord server](https://discord.gg/JCaqAvapGR)'s #api chat for suggestions, errors, updates, etc.
