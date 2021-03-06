# Merge SCSS

Merges an SCSS file and all of its imports together.

## Installation

`yarn add -D @highpoint/merge-scss`

## Usage

In your package.json file's `scripts` section, add a script similar to this:

`"merge-scss": "merge-scss --in css/main.scss --out dist/bundle.scss"`

Alternatively, use as a module in your project like this:

```javascript
const fs = require('fs');
const mergeSCSS = require('@highpoint/merge-scss');

mergeSCSS('./main.scss')
  .then(scss => fs.writeFileSync('./dist/out.scss', scss));
```
