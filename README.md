[![npm version](https://badge.fury.io/js/ng2-color-picker.svg)](https://badge.fury.io/js/ng2-color-picker) [![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php) [![Dependency Status](https://www.versioneye.com/nodejs/ng2-color-picker/0.1.12/badge?style=flat-square)](https://www.versioneye.com/nodejs/ng2-color-picker/0.1.12) [![Build Status](https://travis-ci.org/AndyMeps/ng2-color-picker.svg?branch=master)](https://travis-ci.org/AndyMeps/ng2-color-picker)

[![NPM](https://nodei.co/npm/ng2-color-picker.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/ng2-color-picker/)

# ng2-color-picker

Simple color picker for Angular 2

![Screenshot open](https://raw.githubusercontent.com/AndyMeps/ng2-color-picker/master/assets/screenshot-color-picker-open.png)

## Dependencies

The module relies on `ng2-bootstrap` for dropdown functionality.

## Installation

To include in your project install via NPM with:

```
npm install --save ng2-color-picker
```

You will then need to include the module to your app.module.ts:

```typescript
import { ColorPickerModule } from 'ng2-color-picker';

// ...

@NgModule({
    imports: [
        ColorPickerModule
    ]
})
///...
```

Finally, include the component in your HTML as per the next section.

## HTML Component Markup

Once the module is installed, you will need to add HTML markup to include the picker in a component.
The minimum requirement is an [(ngModel)] attribute, which should provide a string representation of a color.

```html
<color-picker
    [(ngModel)]="color">
</color-picker>
```

It is possible to configure `ng2-color-picker` by providing a configuration object to the `[pickerConfig]` attribute (see the next section for more details on this object):

```html
<color-picker
    [(ngModel)]="color"
    [pickerConfig]="pickerOptions">
</color-picker>
```

## Configuration

`ng2-color-picker` exposes an interface to provide an indication of valid configuration properties, this can be referenced as a type for your configuration object by importing it:

```typescript
import { IPickerConfiguration } from 'ng2-color-picker';
```

Which can then be used as the configuration object type in your component:

```typescript
public pickerOptions: IPickerConfiguration;
```

Current list of configuration options, types and default values:

| Property | Type | Default | Description. |
| -------- | ---- | ------- | ------------ |
| width | `number` | 25 | Width of the picker control. |
| height | `number` | 25 | Height of the picker control. |
| borderRadius | `number` | 4 | Radius of the picker control border. |
| availableColors | `string[]` | `['#f00', '#0f0', '#00f']` | Default list of colors available from the dropdown menu. |