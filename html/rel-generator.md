
# `rel=generator`

HTML already offers a way to indicate the generator software of a Web page using meta names (see [HTML Standard §generator](https://html.spec.whatwg.org/multipage/semantics.html#meta-generator)). However, this invites authors to define said generator as a string of text. To me, this seems a bit silly, as the whole idea of hypertext markup is to link data in a meaningful way. I therefore propose adding ``generator`` as a link relation as well.

## Examples

### With Title

```html
<link rel="generator" href="https://www.jetbrains.com/phpstorm/" title="PhpStorm: The PHP IDE by JetBrains">
```

## Without title

```html
<link rel="generator" href="https://www.adobe.com/products/dreamweaver.html">
```
## In conjunction with meta name

Perhaps useful when considering backwards compatability with user agents that implemented mechanisms for the existing meta name.

```html
<meta name="generator" content="Adobe Dreamweaver">
<link rel="generator" href="https://www.adobe.com/products/dreamweaver.html">
```
