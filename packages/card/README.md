## Description

An `<sp-card>` represents a rectangular card that contains
a variety of text and image layouts. Cards are typically used
to encapsulate units of a data set, such as a gallery of
image/caption pairs.
Spectrum has several card variations for different uses.

### Usage

[![See it on NPM!](https://img.shields.io/npm/v/@spectrum-web-components/card?style=for-the-badge)](https://www.npmjs.com/package/@spectrum-web-components/card)
[![How big is this package in your project?](https://img.shields.io/bundlephobia/minzip/@spectrum-web-components/card?style=for-the-badge)](https://bundlephobia.com/result?p=@spectrum-web-components/card)

```
yarn add @spectrum-web-components/card
```

Import the side effectful registration of `<sp-card>` via:

```
import '@spectrum-web-components/card/sp-card.js';
```

When looking to leverage the `Card` base class as a type and/or for extension purposes, do so via:

```
import { Card } from '@spectrum-web-components/card';
```

## Example

```html demo
<sp-card title="Card title" subtitle="JPG">
    <img alt="" slot="cover-photo" src="https://picsum.photos/200/300" />
    <div slot="footer">Footer</div>
</sp-card>
```

## Title

By default, the title for an `sp-card` is applied via the `title` attribute, which is restricted to string content only. When HTML content is desired, a slot named `title` available for applying the title.

```html demo
<sp-card subtitle="JPG">
    <h1 slot="title">Card title</h1>
    <img alt="" slot="cover-photo" src="https://picsum.photos/200/300" />
    <div slot="footer">Footer</div>
</sp-card>
```

## Variants

There are multiple card variants to choose from in Spectrum. The `variant`
attribute controls the main variant of the card.

### Normal

Normal cards can contain a title, a subtitle, a cover photo, and a footer.

```html
<sp-card title="Card title" subtitle="JPG">
    <img alt="" slot="cover-photo" src="https://picsum.photos/200/300" />
    <div slot="footer">Footer</div>
</sp-card>
```

### Quiet

Quiet cards can contain a title, a subtitle, a cover photo, a description, and a footer.

```html
<div style="width: 208px; height: 264px">
    <sp-card variant="quiet" title="Card title" subtitle="JPG">
        <img alt="" slot="preview" src="https://picsum.photos/200/300" />
        <div slot="description">10/15/18</div>
        <div slot="footer">Footer</div>
    </sp-card>
</div>
```

### Gallery

Gallery cards can contain a title, a subtitle, an image preview, a description, and a footer.

```html
<div style="width: 532px; height: 224px">
    <sp-card variant="gallery" title="Card title" subtitle="JPG">
        <img
            alt=""
            slot="preview"
            src="https://picsum.photos/532/192"
            style="object-fit: cover"
        />
        <div slot="description">10/15/18</div>
        <div slot="footer">Footer</div>
    </sp-card>
</div>
```
