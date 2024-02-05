# Entry Structure



## Word Class
Valid word classes are:

- root
- proper word
- derived
- phrase
- affix

## Etymology



## Rhymes

All entries except phrases should list rhymes. All rhyme words should be in a single list, alphabetically sorted. (Not segmented by strong rhymes, weak rhymes, etc. By popularity would be neat, but we don't have the data to do that even if we wanted to.)

> [!NOTE]
> In this section:
>
> - root will mean root or proper word term
> - derived will mean derived or phrase term
> - last morphme means the final term in a derived terms etymology or the root term itself for a root
> - root/affix alt form is for terms like `kal` and `-kal` which are alternative forms of eachother.

Our working minimum algorithm for a rhyme is:

> The last two letters must be the same, but if the last two letters are consonants then it must be at least the last three letters.

But while listing rhymes of a entry, there are several rules of when not to list a rhyming term. They are:

1. Don't list non-word terms (non-roots).

    1. Don't list rhyming phrases that rhyme with this entry. (Eg. `kom` should not list `alo kom`.)
    2. Don't list rhyming affixes that rhyme with this entry. (Eg. `sen` should not list `-yen`.)
       
2. Don't show derived words that share the same last morpheme as this entry.
   
    1. If this entry is a root/proper word, don't list derived terms that use this entry as the last morpheme. (Eg. `kom` should not list `nonkom`.)
    2. If this entry is a derived word, don't list a derived terms that uses this entry's last morpheme as the rhyming term's last morpheme. (It doesn't matter if the two final morphemes rhyme.) (Eg. `Kanadayen` shouldn't list any other nationality ending with `-yen`.)
     
3. Don't show terms that are the root/affix form of this entry.

    1. If this entry is a root/proper word, don't list rhyming derived terms where the final morphmeme is the affix form of this entry. (Eg. `kal` shouldn't show words ending with + `-kal`.)
    2. If this entry is derived and the last morpheme is an affix, don't list rhyming terms where last morpheme is the root form if this entry. (Eg. Entries ending with `-kal` shouldn't show terms with the last morpheme `kal`)
    3. Conversely, if this entry is derived and the last morpheme is a root/proper word, don't list rhyming terms where last morpheme is the affix form if this entry. (Eg. Entries ending with `kal` shouldn't show terms with the last morpheme `-kal`)

Use the heading `Rhyming Words not Ending in %1$s` and list the final morpheme of this term, and the root/affix alt version, if there is one.



Entries to run tests on to make sure this is working properly:
- `kom` should not list terms ending with `kom' (2i. Eg. `nenkom`)
- `kom' should not list phrases, eg. `alo kom` (1i.)
- `Kanadayen` should not list other nationalities (2ii. Ending with -yen)
- 1ii: ?
- 3i: ?
- 3ii: ?
- 3iii: ?


