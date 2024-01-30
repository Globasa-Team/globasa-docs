# API 2

API 2 is currently still in development. The standard translations file contains the word class, category, translations and etymology for each term in the dictionary.

- https://cdn.globasa.net/api2/standard.json
- https://cdn.globasa.net/api2/standard.yaml

The standard definition file consists of an indexed array by term slug, each with basic properties and all translations for each word.

## Structure

The array is indexed by the term slug. Each element contains:

- `word class`: string
- `category`: string
- `trans`: array of 3-letter language code keys => array of translations
  - $lang: array of translations
- `etymology`
  - `derived`: array of morphemes and connector symbols
  - `natlang`: array of $lang=>$terms key/value pairs
  - `am oko`: array of terms
  - `a priori`: boolean
  - `kwasilexi`: array of $lang=>$terms key/value pairs
  - `am kompara`: array of terms
  - `link`: string (url)


## Examples
```
{
  "komputatora":{
     "word class":"b",
     "category":"derived",
     "trans":{
        "eng":[
           [
              "computer"
           ]
        ],
        "epo":[
           [
              "komputilo"
           ]
        ],
        "spa":[
           [
              "computadora",
              "computador",
              "ordenador"
           ]
        ]
     },
     "etymology":{
        "derived":[
           "komputa",
           "+",
           "-tora"
        ]
     }
  }
}
```
