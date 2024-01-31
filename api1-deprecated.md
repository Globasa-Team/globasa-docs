# Globasa API1 data files

> [!CAUTION]
> These files are no longer updated and are maintained in a new location for people who might not have known they being deprecated.

Globasa dictionary files are updated every night from the official Globasa spreadsheet.

*   [Comma Seperated Value](https://cdn.globasa.net/api1/globasa-basili-menalar-1.csv) (CSV) of the Globasa translation dictionary.
*   [globasa-menalar-1.yaml](https://cdn.globasa.net/globasa-menalar-1.yaml) - Dictionay file encoded as YAML for PHP.
*   [globasa-menalar-1.json](https://cdn.globasa.net/globasa-menalar-1.json) - Dictionary file encoded as JSON for JavaScript.
*   [globasa-menalar-1.js](https://cdn.globasa.net/globasa-menalar-1.js) - JavaScript file that loads dictionary in a variable named `dictionary`.

Question about the data files should be directed to the #api channel of the [Globasa Discord server](https://discordapp.com/invite/x5crvCa) or the #globasa\_multilingual channel of the [auxlang Discord server](https://discord.gg/tyYHheM).

> [!CAUTION]
> These files are no longer updated and are maintained in a new location for people who might not have known they being deprecated.

## APIv1 Structure

This is the structure of the data files.

*   ### `index`
    
    This has a list of all indexes for all languages to fascilate language lookups. It includes the following languages, but more may be added without notice. Talk with the community to discover how complete any language is.
    
    *   `eng`
    *   `spa`
    *   `epo`
    
*   ### `words`
    
    A list of Globasa words and properties for each word. Each word has these properties:
    
    *   `term`
    *   `termIndex`
    *   `category`
    *   `wordClass`
    *   `part`
    *   `etymology`
    *   `relatedWords`
    *   `ipaLink`
    *   `example`
    *   `tags`
    *   `synonyms`
    *   `antonyms`
    *   `status`
    *   `translation`
        *   `eng`
        *   `epo`
        *   `deu`
        *   `fra`
        *   `rus`
        *   `spa`
        *   `zho`
*   ### `derived`
    
    Currently unused. May be used to contain a list of words from derived words in the word list.
    
*   ### `tags`
    
    A list of tags and words with those tags.

> [!CAUTION]
> These files are no longer updated and are maintained in a new location for people who might not have known they being deprecated.
