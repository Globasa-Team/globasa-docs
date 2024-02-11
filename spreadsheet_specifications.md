# Spreadsheet Specifications

Here I will outline the format this script expects for imported CSV data from the Google Sheets.

## Word column
The Word column is the term for this entry.
- TODO: Rename `Word` column to `term`
- TODO: Linter: check that only `WORD_CHARS_REGEX` `'/[^A-Za-z0-9 \-]/'` are present (term parser global constants)

## Entry Note

Entry notes are to be sperated by a period. (Maybe a pipe `|` if ntoes need periods.) Each note needs a keyword phrase followed by a colon. The data contained in the note depends on the colon.

- Am oko: [Globasa term]
- Kurto lexi cel: [Globasa term]
- Am kompara fe: [Globasa term]
- Am oko tabellexi [link to Correlatives in respective natlang]
- Yongudo sol ton: [Globasa term]
- Nota: free form markdown

## Etymology (LexiliAsel)

Break apart the LexiliAsel field around any period. Process each part seperately:

* If blank, then none.
* If it starts with https:// or http://, then URL
* If it contains `(` then it's a `NATLANG`
* Else, it's `DERIVED`

# Source Natlang

Acceptible format:

```
kwasilexi - natlang1 (comments), natlang2 (comments)

natlang1, natlang2 (comment), natlang3

natlang1, natlang2, natlang3
```

* `kwasilexi - ` is an optional start that indicates it's an onomatopoeic word.
* Brackets around a comment are optional.
* natlangs are listed, seperated by commas.

# Derived Etymology

Break apart etymology by spaces. For each 'word'

* If it's a `+` start a new phrase.
* If it's a `,` start a new phrase.
* If it's a `.` start a new phrase.
* If it's an `oko` and followed an `am` then add it to final string
* If it's a priori_ and followed an '_a` then add it tot he final string
* Otherwise, Add the current word to phrase
* unless it's a new phrase, in which case add the phrase so far to the final result and start a new blank phrase.
