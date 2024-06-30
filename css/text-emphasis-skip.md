
# `text-emphasis-skip`

## Syntax

```css
/* Initial value */
text-emphasis-skip: none;

/* <string> values */
text-emphasis-skip: "a";

/* Keyword values */
text-emphasis-skip: capitals;
text-emphasis-skip: consonants;
text-emphasis-skip: lowercase;
text-emphasis-skip: vowels;
```

### Values

<dl>
<dt>`none`</dt>
<dd>No characters skipped.</dd>
<dt>`capitals`</dt>
<dd>All capital characters skipped.</dd>
<dt>`consonants`</dt>
<dd>All consonants skipped.</dd>
<dt>`lowercase`</dt>
<dd>All lowercase characters skipped.</dd>
<dt>`numbers`</dt>
<dd>All numeral characters skipped.</dd>
<dt>`vowels`</dt>
<dd>All vowels skipped.</dd>
</dl>

## Examples

### Dutch Emphasis

```css
em:lang(nl) {
  font-style: normal;
  text-emphasis-style: "\0301";
  text-emphasis-skip: capitals vowels "ij";
}
```
