# dynamic-qr-code-generator

<img src="https://img.shields.io/badge/Licence-MIT-blue.svg" alt="Licence" data-canonical-src="https://img.shields.io/badge/Licence-MIT-blue.svg" style="max-width:100%;"/>
<img src="https://img.shields.io/badge/Version-0.0.2-brightgreen.svg" alt="npm Version" data-canonical-src="https://img.shields.io/badge/Version-0.0.2-brightgreen.svg" style="max-width:100%;"/>

A vanilla javaScript based NPM package that generate QR code with logo and customisable options. Also give a better user experience with better and flexible options/features.

# Demo and Docs

* Inspired by [npm link](https://www.npmjs.com/package/qrjs2)

* Click [here](https://technologygeek12.github.io/qr-code-generator/) for [Live Demo](https://technologygeek12.github.io/qr-code-generator/)

## Installation
The package can be installed via NPM:

```javascript
npm install dynamic-qr-code-generator --save

yarn add dynamic-qr-code-generator
```
dynamic-qr-code-generator can be imported as follows

```javascript
var {QRGenerator} = require('dynamic-qr-code-generator');

OR

import {QRGenerator} from 'dynamic-qr-code-generator';

```



# Examples


## Basic Example with all default props

```javascript
import {QRGenerator} from 'dynamic-qr-code-generator';

var props={value:'Your text or URL here'};

return (
        <div id="qr-container"></div>
        <button onClick={()=>QRGenerator(props)}>generate</button>
);

```

## Basic Example to show logo in QR code

```javascript
import {QRGenerator} from 'dynamic-qr-code-generator';

var props={isLogo:true,value:'Your text or URL here'};

return (
        <div id="qr-container"></div>
        <button onClick={()=>QRGenerator(props)}>generate</button>
        <img id='qr-logo-image' src={home} style={{ display: 'none' }} />
);

```

## Basic Example to set height width of QR code

```javascript
import {QRGenerator} from 'dynamic-qr-code-generator';

var props={width:256,height:256,value:'Your text or URL here'};

return (
        <div id="qr-container"></div>
        <button onClick={()=>QRGenerator(props)}>generate</button>
);

```

## Basic Example to set width of logo in QR-code

```javascript
import {QRGenerator} from 'dynamic-qr-code-generator';

var props={isLogo:true,logoSize:80,value:'Your text or URL here'};

return (
        <div id="qr-container"></div>
        <button onClick={()=>QRGenerator(props)}>generate</button>
        <img id='qr-logo-image' src={home} style={{ display: 'none' }} />
);

```

## Basic Example to set background or forground color of QR-code

```javascript
import {QRGenerator} from 'dynamic-qr-code-generator';

var props={backgroundColor:'#fff',foregroundColor:'#000',value:'Your text or URL here'};

return (
        <div id="qr-container"></div>
        <button onClick={()=>QRGenerator(props)}>generate</button>
);

```

## Basic Example with all default props in React

```jsx
import React, { Component } from 'react';
import {QRGenerator} from 'dynamic-qr-code-generator';

class App extends Component {

  render() {
      var props={backgroundColor:'#fff',foregroundColor:'#000',width:256,height:256,isLogo:true,logoSize:80,customLogoDesign:false,value:'Your text or URL here'}
    return (
      <div>
        <div id="qr-container"></div>
        <button onClick={()=>QRGenerator()}>generate</button>
        <img id='qr-logo-image' src={home} style={{ display: 'none' }} />
      </div>
    );
  }
}

export default App;

```

# Default parameter options value
```javascript
    backgroundColor:'#fff',
    foregroundColor:'#000',
    width:256,
    height:256,
    isLogo:false,
    logoSize:80,
    customLogoDesign:false,
    value:'https://github.com/TechnologyGeek12/qr-code-generator'
```

# Available options list
```javascript
    backgroundColor:String,
    foregroundColor:String,
    width:Number,
    height:Number,
    isLogo:Boolean,
    logoSize:Number,
    customLogoDesign:Boolean,
    value:String     
```

The word 'QR Code' is registered trademark of DENSO WAVE INCORPORATED 
[Check here](http://www.denso-wave.com/qrcode/faqpatent-e.html)