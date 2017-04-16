# cn decorator

[![Build Status](https://travis-ci.org/alfa-laboratory/cn-decorator.svg?branch=master)](https://travis-ci.org/alfa-laboratory/cn-decorator)

Best way to use BEM with React

## Features

* [BEM methodology for React](#bem-react)
* [Themes management](#themes)
* [`className` proxy](#className)
* [BEM overrides](#overrides)
* [DI Components](#di-components)

## BEM methodology for React <a href="#bem-react"></a>

`cn decorator` provides simplest ability to generate BEM methodology classes inside React Component.

### Basic example

```javascript
import cn from 'cn-decorator';
import React from 'react';
import './my-component.css';

@cn('block-name')
class MyComponent extends React.Component {
    render(cn) {
        return <div className={ cn } />;
    }
}

// Render result:
// <div class="block-name"></div>
```

### Use for elements

```javascript
import cn from 'cn-decorator';
import React from 'react';
import './my-component.css';

@cn('block-name')
class MyComponent extends React.Component {
    render(cn) {
        return (
            <div className={ cn }>
                <span className={ cn('some-element') } />
            </div>
        );
    }
}

// Render result:
// <div class="block-name">
//     <span class="block-name__some-element"></span>
// </div>
```

### Add mods

```javascript
import cn from 'cn-decorator';
import React from 'react';
import './my-component.css';

@cn('block-name')
class MyComponent extends React.Component {
    render(cn) {
        return <div className={ cn({ mod1: true, mod2: 'value' }) } />;
    }
}

// Render result:
// <div class="block-name block-name_mod1 block-name_mod2_value"></div>
```

## Mods for elements

```javascript
import cn from 'cn-decorator';
import React from 'react';
import './my-component.css';

@cn('block-name')
class MyComponent extends React.Component {
    render(cn) {
        return (
            <div className={ cn }>
                <span className={ cn('some-element', { mod1: true }) } />
            </div>
        );
    }
}

// Render result:
// <div class="block-name">
//     <span class="block-name__some-element block-name__some-element_mod1"></span>
// </div>
```

## Themes management <a href="#themes"></a>

## `className` proxy <a href="#className"></a>

## BEM overrides <a href="#className"></a>

## DI Components <a href="#di-components"></a>

## License

```
The MIT License (MIT)

Copyright (c) 2017 Alfa Laboratory

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
