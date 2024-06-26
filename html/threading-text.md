
# Threading Text

## Introduction

Hypertext currently has no mechanism to have (text) content flow into a different container when the initial container runs out of space. This has been an indispensable feature of desktop publishing software like [InDesign](https://helpx.adobe.com/indesign/using/threading-text.html) for decades, and is clearly missing from Web publishing.

## Why HTML

This might feel like a feature that should be handled by CSS, as it concerns a visual representation. In fact, if an HTML document has no styling applied to it at all, chances are the initial container stretches with the (text) content, and the feature is irrelevant. However, what content goes into which container is a structural and semantic endeavor, and so is threading containers together.

## Markup

```HTML
<div class="box" id="box-1" thread="box-2">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing 
        elit. Ad, adipisci aperiam, asperiores aspernatur 
        cupiditate dolor eaque exercitationem facilis ipsa 
        iusto laboriosam laudantium obcaecati quibusdam 
        quisquam, recusandae repellendus sit tempore ut.</p>
</div>

<div class="box" id="box-2" thread="box-3"></div>

<div class="box" id="box-3"></div>
```
## Styling

Although the focus of this proposal is on markup because of the structural and semantic nature, a complementary CSS proposal could allow end-users to opt in to the proposed visual  representation, and offer fall-backs. 

```CSS
.box {
    overflow: thread, hidden;
}
```
