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
  - $lang: array of translation groups
    - array of translation strings (for first group)
    - \[... n arrays of translations\]
- `etymology`: array of one or multiple elements
  - `derived`: array of morphemes and connector symbols
  - `natlang`: array of $lang=>$terms key/value pairs
  - `am oko`: array of terms
  - `a priori`: boolean
  - `kwasilexi`: array of $lang=>$terms key/value pairs
  - `am kompara`: array of terms
  - `link`: string (url)


## Examples

### Derived Etymology
```json
  "komputatora":{
     "word class":"b",
     "category":"derived",
     "trans":{
        "eng":[
           ["computer"]
        ],
        "epo":[
           ["komputilo"]
        ],
        "spa":[
           ["computadora","computador","ordenador"]
        ]
     },
     "etymology":{
        "derived":["komputa","+","-tora"]
     }
  },
```

### Natlang Etymology
```json
  "absorbi":{
      "word class":"b.oj",
      "category":"root",
      "trans":{
         "eng":[
            ["absorption"],
            ["absorb"]
         ],
         "epo":[
            ["sorbo","absorbo"],
            ["sorbi","absorbi"]
         ],
         "spa":[
            ["absorci\u00f3n"],["absorber"]
         ]
      },
      "etymology":{
         "natlang":{
            "Doycisa":"Absorption; absorbieren",
            "Englisa":"absorption, absorbing; absorb",
            "Espanisa":"absorci&oacute;n; absorber",
            "Fransesa":"absorption; absorber",
            "Indonesisa":"absorpsi",
            "Italisa":"assorbimento; assorbire",
            "Pilipinasa":"absorpsiyon",
            "Portugalsa":"absor&ccedil;&atilde;o; absorver",
            "Rusisa":"\u0430\u0431\u0441\u043e\u0440\u0431\u0446\u0438\u044f &ldquo;abs&oacute;rbtsyiya&rdquo;",
            "Turkisa":"absorpsiyon"
         }
      }
   },
```

### Natlang and Kwasilexi etymology

```json
   "bwaw":{
      "word class":"b",
      "category":"root",
      "trans":{
         "eng":[
            ["dog","<em>Canidae<\/em>"]
         ],
         "epo":[
            ["hundo"]
         ],
         "spa":[
            ["perro","<em>Canis lupus familiaris<\/em>"]
         ]
      },
      "etymology":{
         "natlang":{
            "Swahilisa":"mbwa"
         },
         "kwasilexi":{
            "Arabisa":"\u0647\u0648 \u0647\u0648 &ldquo;hau hau&rdquo;",
            "Banglasa":"\u09ad\u0989 \u09ad\u0989 &ldquo;bhou bhou&rdquo;",
            "Bulgarisa":"\u0431\u0430\u0443 \u0431\u0430\u0443 &ldquo;bau bau&rdquo;",
            "Doycisa":"wau wau",
            "Englisa":"bow wow",
            "Espanisa":"guau guau",
            "Hervatskasa":"vau vau",
            "Pilipinasa":"aw aw",
            "Telugusa":"\u0c2d\u0c4c \u0c2d\u0c4c &ldquo;bhau bhau&rdquo;"
         }
      }
   },
```
