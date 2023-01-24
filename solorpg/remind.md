Use the following steps:
1. Download a copyright free book from Gutenberg.org (for example)
2. Remove front and end matter not related to narrative. Also remove chpater headings.
3. Change all non-letters to spaces. In vim, I use `:%s/[^0-9A-Za-zÀ-ÖØ-öø-ÿ ]/ /g`. It may be necessary to add postrophe and/or remove digits.
4. Make sure the file is in the correct file format using `:set fileformat=unix`
5. Save and use tr to change all newlines to spaces: `tr '\n' ' ' < OLDNAME > NEWNAME
6. Again in vim, consolidate all whitespaces: `:%s/\s\+/ /g`
7. Break after every five words: `:%s:\(\w\+ \w\+ \w\+ \w\+ \w\+\) :\r:g`
8. Whatever further cleanup may be necessary.
