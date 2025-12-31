<!--
SPDX-FileCopyrightText: 2022 Siemens AG

SPDX-License-Identifier: MIT
-->

![iX](./logo.svg)

> Siemens Industrial Experience Icons

[![License: SEE LICENSE IN <LICENSE.md>](https://img.shields.io/badge/License-SEE%20LICENSE%20IN%20LICENSE.md-yellow.svg)](./LICENSE.md)

## Usage

### Setting up with Siemens Industrial Experience design system

If you are also using the library [Siemens Industrial Experience](https://github.com/siemens/ix/), no additional project setup will be necessary. The packages `@irisieason/ix-angular`, `@irisieason/ix-react` or `@irisieason/ix-vue` will take care of setting up the icon library for you.

### Setting up without Siemens Industrial Experience design system

If you want to use `@irisieason/ix-icons` without `@irisieason/ix` you need to follow these steps:

#### Using CDN

Place the following `<script>` near the end of your page, right before the closing </body> tag.

```html
<script type="module" src="https://cdn.jsdelivr.net/npm/@irisieason/ix-icons@%5E3.0.0/dist/ix-icons/ix-icons.esm.js"></script>
<script nomodule src="https://cdn.jsdelivr.net/npm/@irisieason/ix-icons@%5E3.0.0/dist/ix-icons/ix-icons.js"></script>
```

Now you can render icons in your applicaton:

```html
<ix-icon name="star"></ix-icon>
```

### Using a package manager like `npm`/`pnpm`/`yarn`

First install the package `@irisieason/ix-icons@latest` in your project (e.g. `npm install --save @irisieason/ix-icons`).

Then load the icon component:

```javascript
import { defineCustomElements } from '@irisieason/ix-icons/loader';

// Register Web Component <ix-icon></ix-icon>
defineCustomElements();
```

### Prepare your project

1. **Copy SVG Files:**
   Copy all SVG files located under `node_modules/@irisieason/ix-icons/svg` to an asset folder in your project. This allows the `ix-icon` component to fetch the images.

2. **Alternative Method:**
   Alternatively, you can use the `addIcons` function to load specific icons directly in your code. For example:

   ```javascript
   import { addIcons } from '@irisieason/ix-icons';
   import { iconStar } from '@irisieason/ix-icons/icons';

   addIcons({ iconStar });
   ```

   ```html
   <ix-icon name="star"></ix-icon>
   ```

   You only need to add the same icon once. Additional calls to `addIcons` will not add redundant copies of the same icons to the collection.

### Use the `ix-icon` component with custom SVG's

```tsx
<ix-icon name="/your/asset/path/my-icon.svg"></ix-icon>
```

## Development

### Installation

```sh
pnpm install
```

### Build

```sh
pnpm build
```

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

## 📝 License

Copyright © 2019–2025 [Siemens AG](https://www.siemens.com/).

This project is MIT licensed.
