<p align="center">
  <img src="https://github.com/createnextapp/react-barcode/blob/master/README/logo.png" alt="react-barcode" />
  <p>
    [![NPM](https://img.shields.io/npm/v/@createnextapp/react-barcode.svg)](https://www.npmjs.com/package/@createnextapp/react-barcode) [![downloads](https://img.shields.io/npm/dm/@createnextapp/react-barcode.svg?style=flat-square)](https://www.npmjs.com/package/@createnextapp/react-barcode) ![npm bundle size](https://img.shields.io/bundlephobia/min/@createnextapp/react-barcode) [![Build Status](https://api.travis-ci.com/Bunlong/@createnextapp/react-barcode.svg?branch=master)](https://travis-ci.com/Bunlong/@createnextapp/react-barcode) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
  </p>
</p>

# react-barcode

React component to generate Barcode.

## 🎁 Features

* Compatible with both JavaScript and TypeScript
* Generate as SVG, Canvas and Image
* Support multiple barcodes format

### Barcodes Format

* [CODE128](https://github.com/createnextapp/react-barcode/wiki/CODE128)
  * CODE128 (automatic mode switching)
  * CODE128 A/B/C (force mode)
* [EAN](https://github.com/createnextapp/react-barcode/wiki/EAN)
  * EAN-13
  * EAN-8
  * EAN-5
  * EAN-2
  * UPC (A)
  * UPC (E)
* [CODE39](https://github.com/createnextapp/react-barcode/wiki/CODE39)
* [ITF](https://github.com/createnextapp/react-barcode/wiki/ITF-14)
  * ITF
  * ITF-14
* [MSI](https://github.com/createnextapp/react-barcode/wiki/MSI)
  * MSI10
  * MSI11
  * MSI1010
  * MSI1110
* [Pharmacode](https://github.com/createnextapp/react-barcode/wiki/pharmacode)
* [Codabar](https://github.com/createnextapp/react-barcode/wiki/codabar)

## 🔧 Install

react-barcode is available on npm. It can be installed with the following command:

```
npm install --save @createnextapp/react-barcode
```

react-barcode is available on yarn as well. It can be installed with the following command:

```
yarn add @createnextapp/react-barcode
```

## 💡 Usage

### SVG

```js
import React from 'react';
import { useBarcode } from '@createnextapp/react-barcode';

function App() {
  const [inputRef] = useBarcode({
    value: '1234',
    options: {
      text: 'Hi'
    },
  });
  
  return <svg ref={inputRef} />;
};

export default App;
```

### Canvas

```js
import React from 'react';
import { useBarcode } from '@createnextapp/react-barcode';

function App() {
  const [inputRef] = useBarcode({
    value: '1234',
    options: {
      text: 'Hi'
    },
  });
  
  return <canvas ref={inputRef} />;
};

export default App;
```

### Image

```js
import React from 'react';
import { useBarcode } from '@createnextapp/react-barcode';

function App() {
  const [inputRef] = useBarcode({
    value: '1234',
    options: {
      text: 'Hi'
    },
  });
  
  return <img ref={inputRef} />;
};

export default App;
```

## Parameters

<table>
  <thead>
    <tr>
      <th>Prop</th>
      <th>Type</th>
      <th>Require</th>
      <th>Description</th>
    </tr>
  <thead>
  <tbody>
    <tr>
      <td>value</td>
      <td>string</td>
      <td>✔️</td>
      <td>Text to generate.</td>
    </tr>
    <tr>
      <td>options</td>
      <td>options</td>
      <td>❌</td>
      <td>Barcode options.</td>
    </tr>
  </tbody>
</table>

## Options

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Type</th>
      <th>Default</th>
      <th>Require</th>
      <th>Description</th>
    </tr>
  <thead>
  <tbody>
    <tr>
      <td>format</td>
      <td>string?</td>
      <td><code>auto</code></td>
      <td>❌</td>
      <td>Select which barcode type to use. Please check the <a href="https://github.com/createnextapp/react-barcode/wiki">wikipage</a> of the different barcode types for more information.</td>
    </tr>
    <tr>
      <td>width</td>
      <td>number?</td>
      <td><code>2</code></td>
      <td>❌</td>
      <td>The width option is the width of a single bar.</td>
    </tr>
    <tr>
      <td>height</td>
      <td>number?</td>
      <td><code>100</code></td>
      <td>❌</td>
      <td>The height of the barcode.</td>
    </tr>
    <tr>
      <td>displayValue</td>
      <td>boolean?</td>
      <td><code>true</code></td>
      <td>❌</td>
      <td></td>
    </tr>
    <tr>
      <td>text</td>
      <td>string?</td>
      <td><code>undefined</code></td>
      <td>❌</td>
      <td>Overide the text that is diplayed</td>
    </tr>
    <tr>
      <td>fontOptions</td>
      <td>string?</td>
      <td><code>""</code></td>
      <td>❌</td>
      <td>With fontOptions you can add bold or italic text to the barcode.</td>
    </tr>
    <tr>
      <td>font</td>
      <td>string?</td>
      <td><code>"monospace"</code></td>
      <td>❌</td>
      <td>Define the font used for the text in the generated barcode. This can be any default font or a font defined by a @font-face rule.</td>
    </tr>
    <tr>
      <td>textAlign</td>
      <td>string?</td>
      <td><code>"center"</code></td>
      <td>❌</td>
      <td>Set the horizontal alignment of the text. Can be <code>left</code> / <code>center</code> / <code>right</code>.</td>
    </tr>
    <tr>
      <td>textPosition</td>
      <td>string?</td>
      <td><code>"bottom"</code></td>
      <td>❌</td>
      <td>Set the vertical position of the text. Can be <code>bottom</code> / <code>top</code>.</td>
    </tr>
    <tr>
      <td>textMargin</td>
      <td>number?</td>
      <td><code>2</code></td>
      <td>❌</td>
      <td>Set the vertical position of the text. Can be <code>bottom</code> / <code>top</code>.</td>
    </tr>
    <tr>
      <td>fontSize</td>
      <td>number?</td>
      <td><code>20</code></td>
      <td>❌</td>
      <td>Set the size of the text.</td>
    </tr>
    <tr>
      <td>background</td>
      <td>string?</td>
      <td><code>"#ffffff"</code></td>
      <td>❌</td>
      <td>Set the background of the barcode.</td>
    </tr>
    <tr>
      <td>lineColor</td>
      <td>string?</td>
      <td><code>"#000000"</code></td>
      <td>❌</td>
      <td>Set the color of the bars and the text.</td>
    </tr>
    <tr>
      <td>margin</td>
      <td>number?</td>
      <td><code>10</code></td>
      <td>❌</td>
      <td>Set the space margin around the barcode. If nothing else is set, all side will inherit the margins property but can be replaced if you want to set them separably.</td>
    </tr>
    <tr>
      <td>marginTop</td>
      <td>number?</td>
      <td><code>undefined</code></td>
      <td>❌</td>
      <td></td>
    </tr>
    <tr>
      <td>marginBottom</td>
      <td>number?</td>
      <td><code>undefined</code></td>
      <td>❌</td>
      <td></td>
    </tr>
    <tr>
      <td>marginLeft</td>
      <td>number?</td>
      <td><code>undefined</code></td>
      <td>❌</td>
      <td></td>
    </tr>
    <tr>
      <td>marginRight</td>
      <td>number?</td>
      <td><code>undefined</code></td>
      <td>❌</td>
      <td></td>
    </tr>
    <tr>
      <td>flat</td>
      <td>boolean?</td>
      <td><code>false</code></td>
      <td>❌</td>
      <td>Only for <code>EAN8</code> / <code>EAN13</code></td>
    </tr>
  </tbody>
</table>

## 💖 Wrap Up

If you think any of the `react-barcode` can be improved, please do open a PR with any updates and submit any issues. Also, I will continue to improve this, so you might want to watch/star this repository to revisit.

## 🌟 Contribution

We'd love to have your helping hand on contributions to `react-barcode` by forking and sending a pull request!

Your contributions are heartily ♡ welcome, recognized and appreciated. (✿◠‿◠)

How to contribute:

- Open pull request with improvements
- Discuss ideas in issues
- Spread the word
- Reach out with any feedback

## ⚖️ License

The MIT License [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
