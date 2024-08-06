
# `rel=logo`

The HTML link relation `logo` has been proposed before, but was shot down, mainly because there was already a `rel=icon`. This never made sense to me, as a logo is **not** the same as an icon (although icons are often based off of logos), and associating a logo with a website or page could be beneficial to many authors and organizations on one hand, and various user agents and automated systems like search engines and brand catalogues on the other.

## Reusability

What made ``rel=logo`` not being accepted before even weirder to me, is that the [Atom standard](https://datatracker.ietf.org/doc/html/rfc4287) had already been published at the time. This standard not only defines a [logo element]([logo element](https://datatracker.ietf.org/doc/html/rfc4287#section-4.2.8)), but also explicitly defines how it differs from an icon.

As a graphic designer, I don’t think this definition (of an icon having a 1:1 ratio, and a logo a 2:1 ratio) is perfect by any means[^1], but it is something we can work with. Moreover, as many authors would already have a logo image in place for their Atom feed, referring to the same image with ``rel=logo`` in HTML would be absolutely trivial.

[^1]: In order to improve upon the definition of ``atom:logo``, I would argue that a logo is a rectangle. It could be 2:1 like the current definition of `atom:logo`, it could be 1:1 like `rel=icon`, but it could also be something else. You know, like how actual logos are contained in the real world.

## Example

```html
<link rel="logo" href="https://deidee.com/logo.svg">
```
