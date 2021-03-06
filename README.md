# Angular-Select2-JS-Component

## Related Versions

Angular-Select2-Component is based on these plugins and libs(version):
- [angular(>= 2.0-release)](https://angular.io/)
- [jQuery](https://jquery.com/)
- [select2](https://select2.github.io/)

## How to use
---
### Install
``` cmd
// npm install
npm install angular-select2-js-component --save

// if you have not installed jquery
npm install jquery --save
```

### Use as component
1. Import component.

``` javascript
// import NgModule
import {NgModule} from '@angular/core';
// import Select2Component
import {Select2Component} from 'angular-select2-js-component';

@NgModule({
  // ...
  // declare components
  declarations: [Select2Component]
})
export class YourModule {
}
```

2. Template.

``` html
<select2 [options]="options" [settings]="{ setting: value }" [(ngModel)]="optionSelected" (onSelect)="onSelect($event)"></select2>
```

### Options
- `options`: `option[]`
  - select options for select2
  - `option`: `{id: value, text: key}` or `string`
- `ngModel`: option value that is selected
  - `id` or `string` while multiple is disable
  - `id[]` or `string[]` while multiple is enable
- `onSelect`
  - callback when option selected
  - parmas: `option`(`{id: value, text: key, selected: ifSelected}` or `string`)
- `settings`
  - configurable settings, see [Select2 options API](https://select2.org/configuration/options-api)
  - `setting`: `{ settingOption: value, settingOption: value }`
