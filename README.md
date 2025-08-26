# Globasa Docs

A location for technical documents regarding the API backend, data files, and translation dictionary website views.

> [!NOTE]
> Globasa Team projects use 3-letter language codes when referencing natlang languages.

## API v2 Data Files Documentation

API Location: `https://cdn.globasa.net/api2/`

The Globasa word list backend downloads the Globassa word list spreadsheet, parses that data, and writes out a series of files that can be used by other applications.

### End user files
These files are the unprocessed, raw spreadsheets from the Globasa word list editors.
  * https://cdn.globasa.net/api2/word-list.csv
  * https://cdn.globasa.net/api2/word-list.tsv  

### Standard Translations File

All dictionary terms and key data. See [api2-standard.md](api2-standard.md).

### Globasa Index

For a simple list of all Globasa terms, use the index:

* `index.json`
* `index.yaml`

They contain a key/value lookup where all entries are listed with a value of null, and some terms are listed with value indicating to connoncial term. For example, `ban leli watu` gives the cononcial index/slug `(fe) ban leli watu`, which can be looked up in the translations files.

### Minimal translations files

> [!NOTE]
> These are basic files that contain

Each language has it's own key/value look up file. The key is the index of a word and the value contains the word class in `<em>` tags and the translation. For example, the index `-cu` has a value of `<em>(b.nenoj xfik)</em> <em>intransitive verb marker</em>, become, get, turn (into)`

As of this time, only eng, epo and spa languages are supported:

* `min_eng.json`
* `min_eng.yaml`
* `min_epo.json`
* `min_epo.yaml`
* `min_spa.json`
* `min_spa.yaml`

### Basic translation files

* `basic_eng.json`
* `basic_eng.yaml`
* `basic_epo.json`
* `basic_epo.yaml`
* `basic_spa.json`
* `basic_spa.yaml`

The basic translation files provide most of what one needs to have a functioning app use Globasa. It contains the term as an index, and then sub fields for class, category and translation.

```
kanada:
  class: su n
  category: proper word
  translation: Canada
```

## Participate

Join the [Globasa Discord server](https://discord.gg/JCaqAvapGR)'s #api chat for suggestions, errors, updates, etc.
