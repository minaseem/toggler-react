# toggler-react

[![Build Status](https://travis-ci.org/minaseem/toggler-react.svg?branch=master)](https://travis-ci.org/minaseem/toggler-react)
[![npm](https://img.shields.io/npm/v/toggler-react.svg)](https://www.npmjs.com/package/toggler-react)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)



This is a react toggler. It can be used to build dropdowns, popovers, tooltips.

## Installation

```
npm install toggler-react
```
or
```
yarn add toggler-react
```

## Usage
```jsx harmony
import React, { useState } from 'react';

function Popover () {
  
    const [isVisible, setVisiblity] = useState(false);
    
    return (
        <Toggler
            overrideClass={"disable"}
            onToggle={setVisiblity}
            popoverVisible={isVisible}>
          <Toggler.Field>
            <div>
              <p>Click me to open Popover</p>
            </div>
          </Toggler.Field>
          <Toggler.Popover>
            <div>
              <p>Hi,This is a Popover</p>
            </div>
          </Toggler.Popover>
        </Toggler>
    );
  }
```


### Props

| Property | Type | Required | Description |
|--------------------------|---------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| overrideClass | String | no | This is added as a class to the root of Popover |
| popoverVisible | Boolean | yes | This tells the toggler to show or hide the popover|
| onToggle | Function | yes | This is a function which takes a Boolean parameter and helps in setting the state of **popoverVisible** to either true or false|


